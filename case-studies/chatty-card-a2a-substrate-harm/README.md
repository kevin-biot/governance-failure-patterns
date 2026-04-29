# Case Study — Chatty-Card A2A and Substrate Harm in Transactional Workflows

## Why This Case Exists

Earlier case notes ([`agent-chains`](../agent-chains/), [`agent-topology-coupling-surface`](../agent-topology-coupling-surface/)) treated natural-language peer coupling and agent-agent topology as governance risks supported by published Sentinel material — qualitatively grounded but without a per-event harm-rate measurement on a transactional workflow.

This case adds the missing measurement. A four-agent booking workflow (intake → broker → seat assignment + meal assignment) was run end-to-end across 5 random seeds × 255 customers = 1275 conversations, on the **naive chatty-card A2A** pattern that the market currently treats as the default for A2A-style multi-agent integration. Every tool call, validation result, customer-id-for vs customer-id-about, and ground-truth reconciliation was logged to an audit substrate that survives the run.

The result converts three pre-existing anti-pattern claims from architectural reasoning into measured numerics:

- `AP006 Natural-Language Peer Coupling` — empirical fault rate, cross-agent contamination rate
- `AP012 MCP Direct-to-LLM Tool Coupling` — empirical wrong-action rate at the tool boundary
- a new anti-pattern surfaced by the experiment itself: `AP018 Closed-World Tool Schema Example Anchoring`

## Relevant Classes / Anti-Patterns

- `F001` Formal Transparency Without Foundational Adequacy
- `F003` Entrained Consensus Mistaken for Validation
- `F004` Coupled Reasoning Collapse
- `AP006` Natural-Language Peer Coupling
- `AP010` Capability Discovery as Attack Surface
- `AP012` MCP Direct-to-LLM Tool Coupling
- `AP018` Closed-World Tool Schema Example Anchoring (introduced by this case)

## Provenance Boundary

The full code, audit databases, transcripts, and analytical scripts are currently in a private research repository. **Citable artefacts** for verification:

- Source tag: `d5-v1.1` at commit `817c68d9` in `research/sentinel-validation/phase-d/d5-plane-seat-meal-substrate-harm/`
- Locked pre-registration hash: `ac8c6f66…2146e` (predates the experiment; thresholds and hypotheses fixed before any run)
- Forthcoming: public DOI/Zenodo handle on publication; this README will be updated with the public reference. The commit hash continues to function as a tamper-evident reproducibility check either way.

The numerical values cited below are reproducible from the source tag with the same seed set and the same LM Studio model identifiers.

## Summary Judgment

The bounded claim of this case is:

**Chatty-card A2A — agent cards consulted by an LLM-prose broker, free-text inter-agent briefings, no typed handoff, no state-machine routing — produces a measurable per-customer fault rate of ~96% on a four-agent transactional workflow. The fault rate is robust to model swap within a quality band, to seed variation across five seeds, and to the schema-anchor apparatus correction. The pattern's failure profile sits in the uninsurable region of the Blast Radius Framework (BR-5).**

The pattern's specification base — A2A — is not the problem. A2A's actual specification supports `Task`, `TaskStatus`, `Artifact`, and structured `Part.data` payloads that would refuse most of the failure modes measured here. The problem is that A2A-style agent discovery and chatty inter-agent delegation make it easy and commercially tempting to treat natural-language coordination as if it were a transaction protocol. The naive variant is the market default; the canonical-spec variant is rare.

A v2 canonical-A2A+MCP-per-spec rig has been forked from the same apparatus to measure how much of the fault profile survives strict spec discipline. That measurement is pending; this case study covers v1 (naive) only.

## What the Evidence Shows

### The measured failure profile

Across 5 seeds × 255 customers (n = 1275), with `mistralai/ministral-3-3b` as broker and sub-agents (LM Studio, temperature 0):

| Metric | Value | Interpretation |
|---|---|---|
| Full success (seat reserved AND meal assigned correctly) | 51 / 1275 = **4.0% ± 0.33%** | The pattern almost never completes a transactional workflow correctly |
| Skipped commit (specialist returned without committing) | ~96% per-customer | The chatty broker progresses the workflow on narrative-claimed completion, not on observed state |
| Premature meal events (meal assignment with no reserved seat) | 12 / 20 on smoke (60%) | `assign_meal` is callable when the workflow ledger has no `seat_id` for the customer |
| Cross-customer contamination (smoke) | 35% | Other-customer preferences surface in the active customer's brief |
| Ground-truth violation (smoke, where measurable) | 50% | Where ground truth is available, half of decisions are wrong |
| Sub-agent reserve attempts targeting schema-example seat (`'14A'`) | 19 / 22 | Schema-text anchoring drives default targeting |

The fault rate is consistent across all five seeds (S4 architectural-coupling metric stable at 0.203 ± 0.001). The pattern produces a stable failure attractor, not a high-variance distribution.

### Cross-model invariance disproves model-coupling

A pre-validation smoke on **IBM Granite 4 7B Q8** (different model family, larger, different quantisation) was run on the same 20-customer prefix with the same naive apparatus. Result: Granite produced 19 of 22 reserve attempts targeting the same seat 14A, with the same broker self-confidence about a meal assignment that had no reserved seat. The fault profile was substantially unchanged.

This is informative. It means the failure is not a property of `mistralai/ministral-3-3b`'s training, prior, or alignment — both models read the same `agent_tool_schemas.py` whose example string was `"e.g. '14A' or '32H'"`, and both anchored on it. The pattern is the property of the **architecture**, not of any one model.

### The schema-anchor finding

Changing the schema example from `"e.g. '14A' or '32H'"` to `"e.g. '21F' or '36C'"` (one-character apparatus correction, no other changes) on a 20-customer smoke produced:

- Premature meal events: 12 → **2** (–83%)
- Reserve attempts targeting 14A: 19 → **0**
- Full success rate: 4 → **5** out of 20
- New most-checked seat: **21F** (13 of 46 `check_availability` calls = 28%)

The bias migrated to the new example. The mechanism is stable; the target is mobile. This surfaced a previously uncatalogued anti-pattern (`AP018 Closed-World Tool Schema Example Anchoring`) and required reframing parts of the v1 quantitative claim as apparatus-coupled rather than purely substrate-property. The 96% per-customer fault rate is real, but its decomposition into "substrate failure" vs "schema-anchor confound" required this disambiguation pass to be honest. Without the schema fix, the claim would have overstated substrate.

What survives the schema correction:

- Ground-truth violation rate stays in the same order of magnitude
- Cross-customer contamination via the NL briefing channel is unchanged
- The token ceiling on survivor-narrative length (~6144 chars / ~1536 tokens) is unchanged
- Active vs passive predator differential survival (0% vs 17% on adversarial customers) needs replication on the corrected apparatus before generalising

### What the broker does, observed in transcripts

Cousin's Q1 attribution analysis on premature-meal events found:

- 31% of cases: broker briefing to MealAgent explicitly stated a (fabricated) seat-ready outcome that had not happened ("seat 14A reserved")
- 69% of cases: broker briefing was neutral or even acknowledged seat-pending; MealAgent self-determined to call `assign_meal` anyway
- 0% of cases: a capability or echo failure mode unrelated to the substrate

The first 31% is a broker-side fabrication failure: the chatty broker's narrative state diverged from the ledger state and the divergence wasn't caught because the ledger isn't the routing authority. The 69% is a sub-agent self-determination failure: MealAgent is asked for a structured tool call (`tool_choice="required"`) on the same prompt that says the seat is pending, and complies because the tool boundary has no guard against unmet preconditions.

Both failure modes share the same root substrate: **operational state lives in narrative, not in a typed channel either side is required to consult before acting.**

## Mapping to GFP Anti-Patterns

| Anti-pattern | How chatty-card A2A exhibits it | Empirical signature in this case |
|---|---|---|
| `AP006` Natural-Language Peer Coupling | The broker's free-text briefings to SeatAgent and MealAgent are the operational channel | 35% cross-customer contamination via briefing prose; 31% broker fabrication propagating through unchallenged |
| `AP010` Capability Discovery as Attack Surface | Agent cards advertised in NL are consulted by an LLM-prose broker for routing decisions | Routing decisions occasionally invent specialists or skip required ones; no static guarantee on ordering |
| `AP012` MCP Direct-to-LLM Tool Coupling | `assign_meal` is exposed directly to the LLM with no domain-gate refusing the call when no seat exists | 60% of smoke customers had a meal call attempted on a phantom seat |
| `AP018` Closed-World Tool Schema Example Anchoring | The schema's `description` field carries a concrete example that becomes the default argument | 86% of reserve attempts targeted the schema example seat across two model families |

`AP006` and `AP012` were rated on architectural reasoning before this case. They now have measured per-event rates on a representative transactional workflow. `AP018` is new, surfaced by the apparatus-discipline pass that closed v1.

## Mapping to the Blast Radius Framework

The companion BRF report at [`blast-radius-framework/reports/chatty-card-a2a/`](https://github.com/kevin-biot/blast-radius-framework/tree/main/reports/chatty-card-a2a) rates the chatty-card A2A pattern as **BR-5 (Catastrophic / Uninsurable as deployed)** for transactional workflows.

The rating is driven by:

- **Open-world classifier (framework §4.0):** NL between agents is unbounded substrate; pre-rating gate forces BR-4 floor before per-axis aggregation
- **Invariant 1 (deterministic execution) failing:** the same input produces different routing, different briefings, different tool argument distributions
- **Invariant 7 (bounded coupling) failing:** NL briefing channel is by definition unbounded; `T2` super-additive composition mathematics apply, not `T1` sub-additive
- **Authority axis A4:** broker delegates consequential action (assign meal to wrong customer is a financial / regulatory / dietary-safety event) without external authorisation
- **Coupling axis C4:** natural-language peer coupling is the architecture
- **Reversibility axis V1:** no canary, no rollback; faults commit before detection
- **Observability axis O1:** drift detection on the NL substrate would have to lead the substrate's own faults, which a faster monitor cannot do (per the Phase B Sentinel re-analysis: 20 of 23 experiments crossed G5 yellow inside the baseline-establishment window)

The Kalman uncertainty extension (framework §5.4) is **structurally inapplicable** to this pattern: Invariant 1 fails, so measurement noise R_K cannot be separated from compliance drift, and σ_B(t) cannot be estimated. The pattern is unpriceable as well as unsafe.

## What the Public Evidence Supports

- the 1275-customer fault profile, the cross-model invariance, the schema-anchor disambiguation, and the cousin Q1 attribution decomposition are reproducible from the source tag with the same seeds
- the qualitative claim that "free-text agent-to-agent orchestration without typed gates is unsafe for transactional workflows" is empirically grounded by this case at a scale not previously published

## What This Case Cannot Yet Claim

- whether **canonical A2A+MCP per spec** (typed Tasks, Artifacts, structured `Part.data`, MCP `outputSchema`, domain gates) closes the gaps to ~zero, or leaves measurable residuals — the v2 rig is forked but unrun
- whether AARP / typed-intent substrate replacement adds anything beyond canonical-spec discipline — answerable only after v2 results
- whether the failure profile generalises to longer agent chains (more than four hops) or to non-transactional domains — only the four-hop transactional case is measured here

The honest framing is that this case shows what the **sloppy market default** does when measured carefully, not what A2A-the-specification or MCP-the-specification is capable of when used canonically. The next version of the rig is designed to disambiguate exactly that.

## Relationship to Adjacent Public Work

- [`a2a-coupling-findings`](https://github.com/kevin-biot/a2a-coupling-findings) — public-facing T2 fan-out and Phase B Sentinel re-analysis. The fan-out S4 measurement (0.366, *higher* than either direct broker-to-specialist edge) is a leading indicator for the kind of substrate coupling measured per-event in this case.
- [`blast-radius-framework`](https://github.com/kevin-biot/blast-radius-framework) — the framework against which this case is rated. The rating is in `reports/chatty-card-a2a/`.
- D.5 v2 (private, in-progress) — canonical A2A+MCP per spec; result will sharpen or refute the claim that the failure profile is substrate-driven rather than spec-discipline-driven.

## Demotion Path for a Deployer

A deployer running chatty-card A2A on a transactional workflow today has three live options:

1. **Move to canonical A2A+MCP per spec.** Use `Task`/`TaskStatus`/`Artifact`/`Part.data` for the operational channel. Move RAG / preference-store retrieval into typed `DataPart` payloads. Add MCP `outputSchema` validators that refuse downstream calls when upstream artifacts are absent. Make broker routing a state machine over the ledger, not an LLM prose decision. This may be sufficient — pending v2 measurement.
2. **Move to typed-intent substrate replacement** (AARP-style or equivalent). Replace inter-agent NL with capability requests carrying typed payloads. Specialists respond with typed assertions, not narrative summaries. Whether this adds anything over option 1 is the open question v2/v3 is designed to answer.
3. **Restrict the workflow to advisory action class only.** Where the consequential action surface can be removed (no `assign_meal` equivalent — the LLM advises a human approver), the BR rating drops because Authority A and Reversibility V change. This is an honest demotion path for use cases that don't need execution authority but adopted A2A for the orchestration aesthetic.

Doing nothing is also an option, but the BRF profile makes its consequence visible: BR-5 deployed pattern, structurally unpriceable σ_B(t), explicit AP006 / AP012 / AP018 attestations.
