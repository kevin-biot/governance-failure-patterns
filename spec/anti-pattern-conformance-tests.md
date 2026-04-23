# Anti-Pattern Conformance Tests

*Named challenge procedures for the current governance anti-pattern catalogue.*

**Version:** 0.1
**Date:** 2026-04-23

---

## Purpose

This document gives each anti-pattern one or more stable challenge procedures.

Each test has:

- **Test ID**
- **What it verifies**
- **Procedure**
- **Pass criterion**
- **Evidence mode**

The goal is not fake precision. The goal is repeatable scrutiny.

## How to read results

- `pass` means the anti-pattern was challenged and the system resisted on that
  dimension
- `fail` means the anti-pattern is evidenced on that dimension
- `indeterminate` means the artefacts or instrumentation were not sufficient to
  answer honestly

---

## AP001 — Dashboard Legitimacy Laundering

### AP001-T1 — Normative artefact presence

**Verifies:** whether the dashboard is governed by explicit upstream normative
artefacts rather than functioning as de facto justification.

**Procedure:**
1. Request the normative charter, stakeholder register, and omission register.
2. Check whether those artefacts pre-date the dashboard deployment or scoring
   cycle.
3. Compare the dashboard outputs with those artefacts for consistency.

**Pass criterion:** all three artefacts exist, are versioned, and were not
authored only after the dashboard was already in operational use.

**Evidence mode:** documentary review.

### AP001-T2 — Composite-first presentation check

**Verifies:** whether summary scores are presented before their framing limits.

**Procedure:**
1. Review the dashboard's opening page, executive deck, or public-facing entry
   point.
2. Record whether composite scores or color bands appear before framing,
   omission, and weighting notes.

**Pass criterion:** framing limits and omissions are visible at or before the
first summary score surface.

**Evidence mode:** interface and document inspection.

---

## AP002 — Pooled Baseline Drift Masking

### AP002-T1 — Frozen-baseline replay

**Verifies:** whether deterioration disappears when the reference frame moves
with the system.

**Procedure:**
1. Select a historical period with enough observations to compare.
2. Recompute the monitoring output using:
   - the deployed moving or pooled baseline
   - a frozen external baseline
3. Compare directional conclusions.

**Pass criterion:** materially important deterioration is not erased by the
moving baseline.

**Evidence mode:** replay test.

### AP002-T2 — Absolute vs relative view parity

**Verifies:** whether the system keeps absolute trend views separate from
relative rank views.

**Procedure:**
1. Inspect the reporting outputs.
2. Check whether absolute trend lines are available beside percentile or rank
   views.
3. Check whether important decisions rely only on relative position.

**Pass criterion:** absolute and relative views are both present and neither is
silently substituted for the other.

**Evidence mode:** document and interface inspection.

---

## AP003 — AI Consensus as Validation

### AP003-T1 — Independence challenge

**Verifies:** whether apparent agreement rests on genuinely independent
evidence paths.

**Procedure:**
1. Identify the models, prompt families, source packs, and synthesis loops used
   by each participant or agent.
2. Record how much of that substrate is shared.
3. Check whether the system treats convergence as stronger than its actual
   independence warrants.

**Pass criterion:** agreement is not represented as independent validation when
the evidence path is substantially shared.

**Evidence mode:** architecture and process inspection.

### AP003-T2 — Counter-frame requirement

**Verifies:** whether the process forces a rival framing before treating
convergence as robust.

**Procedure:**
1. Inspect the assessment or policy workflow.
2. Determine whether at least one counter-frame, counter-pack, or rival
   synthesis pass is mandatory.

**Pass criterion:** a counter-frame is required for consequential decisions.

**Evidence mode:** process review.

---

## AP004 — Constitution After the Model

### AP004-T1 — Chronology test

**Verifies:** whether normative governance artefacts were written before the
analytic model became operational.

**Procedure:**
1. Retrieve timestamps or version history for:
   - the model or framework deployment
   - the normative charter
   - stakeholder admissibility and omission artefacts
2. Compare ordering.

**Pass criterion:** the constitutional artefacts pre-date operational scoring
or ranking.

**Evidence mode:** document and version-history review.

### AP004-T2 — Model-authored constitution check

**Verifies:** whether governance language merely ratifies an existing tool.

**Procedure:**
1. Compare constitutional language with the model's existing indicator set,
   weight structure, or category logic.
2. Check whether governance documentation explains why the frame was chosen, or
   only restates the frame already embedded in the tool.

**Pass criterion:** the constitutional layer governs the tool rather than
post-rationalizing it.

**Evidence mode:** documentary and structural comparison.

---

## AP005 — Markov Without Transition-Drift Detection

### AP005-T1 — Transition-drift instrumentation check

**Verifies:** whether the system explicitly monitors transition drift rather
than only emitting state probabilities.

**Procedure:**
1. Inspect the state-model monitoring design.
2. Check for:
   - transition-matrix drift checks
   - residual drift tracking
   - changepoint or regime-break diagnostics

**Pass criterion:** at least one explicit transition-drift diagnostic is in
routine use.

**Evidence mode:** architecture and measurement inspection.

### AP005-T2 — Horizon divergence test

**Verifies:** whether one-step fit hides long-horizon degradation.

**Procedure:**
1. Evaluate short-horizon predictive performance.
2. Evaluate longer-horizon performance or stability.
3. Compare whether the model remains apparently healthy only at short horizon.

**Pass criterion:** no material divergence exists between short-horizon fit and
the system's longer-horizon behavior without a surfaced warning.

**Evidence mode:** replay or validation test.

---

## AP006 — Natural-Language Peer Coupling

### AP006-T1 — Consequential peer-edge mapping

**Verifies:** whether consequential peer-to-peer handoffs are free-form natural
language by default.

**Procedure:**
1. Map the system's peer edges.
2. Identify which edges carry control-relevant content.
3. Classify each edge as:
   - typed or schema-bounded
   - mixed
   - free-form natural language

**Pass criterion:** consequential peer edges are not predominantly free-form
natural language.

**Evidence mode:** architecture inspection.

### AP006-T2 — Coupling under perturbation

**Verifies:** whether agreement and coupling intensify under perturbation while
remaining weakly grounded.

**Procedure:**
1. Run a bounded perturbation, fork, or replay challenge.
2. Observe overlap, repetition, or convergence behavior across peers.
3. Compare the coupling signal with external grounding or truth conditions.

**Pass criterion:** perturbation does not create synchronized convergence or
collapse without external correction.

**Evidence mode:** perturbation test.

### AP006-T3 — Probe dissociation check

**Verifies:** whether internal probes remain green while behavioral quality
degrades.

**Procedure:**
1. Compare internal monitoring or probe success with substantive task quality
   during a challenge run.
2. Record whether probe health and actual behavior diverge.

**Pass criterion:** monitoring and substantive quality remain aligned closely
enough that internal probes are not falsely reassuring.

**Evidence mode:** perturbation or replay test.

---

## AP007 — Policy PDF, Runtime Nothing

### AP007-T1 — Runtime binding check

**Verifies:** whether stated policy constraints are actually bound to runtime
decisions or execution paths.

**Procedure:**
1. Retrieve the governing policy artefacts for the assessed system.
2. Identify at least three consequential policy claims.
3. Trace each claim to a runtime enforcement point or execution record.

**Pass criterion:** each consequential policy claim can be mapped to a live
runtime control, binding, or decision artefact rather than existing only in
documentation.

**Evidence mode:** architecture and document inspection.

### AP007-T2 — Policy challenge replay

**Verifies:** whether a system under challenge behaves according to the policy
it claims to enforce.

**Procedure:**
1. Choose a bounded challenge case that should trigger a policy constraint.
2. Run or replay the case.
3. Compare the runtime outcome to the declared policy behavior.

**Pass criterion:** the runtime system enforces the declared policy outcome
consistently enough that the policy claim survives challenge.

**Evidence mode:** replay or live challenge.

---

## AP008 — Evidence After Action

### AP008-T1 — Preventive-vs-retrospective separation

**Verifies:** whether the system distinguishes preventive controls from
retrospective evidence.

**Procedure:**
1. Review the governance and assurance materials.
2. List the controls the system claims as governance mechanisms.
3. Classify each as:
   - preventive
   - detective
   - retrospective only

**Pass criterion:** the assurance case does not rely on retrospective evidence
alone for consequential control claims.

**Evidence mode:** document and control review.

### AP008-T2 — Fail-closed challenge

**Verifies:** whether the system can actually stop or refuse a consequential
action under a known bad condition.

**Procedure:**
1. Select a challenge condition that should trigger refusal, escalation, or
   halt.
2. Run or replay the case.
3. Observe whether the system blocks the action or merely records it after the
   fact.

**Pass criterion:** the system demonstrates a real preventive response rather
than post-hoc explanation only.

**Evidence mode:** perturbation or replay test.

---

## AP009 — Human Oversight as Ceremony

### AP009-T1 — Oversight quality check

**Verifies:** whether human oversight is instrumented for effectiveness rather
than nominal presence.

**Procedure:**
1. Review approval timing, refusal rates, escalation paths, and evidence
   surfaces available to reviewers.
2. Determine whether the reviewer can realistically inspect what matters before
   approving.

**Pass criterion:** oversight quality is measured and the reviewer has enough
time and evidence to make a meaningful intervention.

**Evidence mode:** process and interface review.

### AP009-T2 — Human intervention drill

**Verifies:** whether the human can actually stop a meaningful failure mode in
practice.

**Procedure:**
1. Run a bounded drill or replay involving a consequential edge case.
2. Put the reviewer in the standard interface and timing conditions.
3. Record whether the reviewer can detect and stop the failure.

**Pass criterion:** the review path supports real detection and interruption of
the challenged failure mode.

**Evidence mode:** drill, replay, or live exercise.

---

## AP010 — Capability Discovery as Attack Surface

### AP010-T1 — Discovery-before-auth check

**Verifies:** whether capability discovery occurs before strong authentication,
principal scoping, or bounded authorization are established.

**Procedure:**
1. Inspect how one agent discovers another agent's capabilities.
2. Determine whether discovery is:
   - public or broadly reachable
   - authenticated but not principal-scoped
   - principal-scoped and policy-mediated
3. Record whether meaningful tool information is disclosed prior to bounded
   execution authority.

**Pass criterion:** capability discovery is authenticated, principal-scoped,
and does not expose more actionable surface than the caller is already
authorized to use.

**Evidence mode:** architecture and protocol inspection.

### AP010-T2 — Semantic-binding check

**Verifies:** whether discovered capabilities are described through typed,
version-bound semantic contracts rather than broad narrative descriptions.

**Procedure:**
1. Review the capability advertisement or discovery payload.
2. Check whether callable actions are defined with:
   - explicit schema
   - version-bound semantics
   - bounded scope and parameter constraints
3. Compare that with any free-form descriptive layer.

**Pass criterion:** discovered capabilities are primarily governed by typed,
versioned semantics and bounded scope rather than by interpretive natural
language alone.

**Evidence mode:** protocol and document inspection.

### AP010-T3 — Enumeration-to-exploitation challenge

**Verifies:** whether the discovery surface materially helps a peer or attacker
shape prompts, requests, or attack paths against the exposed tool set.

**Procedure:**
1. Use the advertised capability surface to construct bounded challenge cases.
2. Attempt prompt shaping, tool overreach, or unauthorized invocation paths
   based on what the discovery layer revealed.
3. Compare results with a control case where the discovery surface is hidden or
   reduced.

**Pass criterion:** discovery does not materially expand the attacker's or
peer's ability to shape or exploit the tool surface beyond their authorized
scope.

**Evidence mode:** adversarial challenge or controlled replay.

---

## AP011 — Rulebook Without Doctrine

### AP011-T1 — Enduring-objective check

**Verifies:** whether the assessed policy stack is governed by an explicit
enduring objective rather than by a collection of locally justified measures.

**Procedure:**
1. Review the major policy, strategy, and implementation documents in scope.
2. Check whether they share a stable statement of:
   - enduring objective
   - principal threat, contradiction, or strategic tension
   - ranked trade-offs when objectives conflict
3. Compare whether later documents preserve or quietly replace that logic.

**Pass criterion:** the stack contains a stable doctrinal core that persists
across instruments and is strong enough to rank trade-offs consistently.

**Evidence mode:** document and cross-instrument review.

### AP011-T2 — Cross-instrument coupling check

**Verifies:** whether new instruments are justified by their fit within a
coherent doctrine rather than only by local administrative purpose.

**Procedure:**
1. Select several linked instruments, including at least one later repair,
   simplification, or omnibus-style measure.
2. Inspect whether each explains:
   - how it fits the wider stack
   - what trade-off rule it inherits
   - what contradiction it resolves upstream
3. Record where coupling has to be inferred after the fact.

**Pass criterion:** cross-instrument coherence is explicit enough that later
repair measures are not doing the work of an absent doctrine.

**Evidence mode:** policy-stack analysis.

### AP011-T3 — Remediation-as-symptom check

**Verifies:** whether simplification or repair packages are functioning as ex
post compensation for deeper uncoupled policy accumulation.

**Procedure:**
1. Identify omnibus, simplification, or implementation-repair measures.
2. Review the stated reason for their existence.
3. Assess whether they mainly:
   - operationalize an already coherent doctrine, or
   - reconcile tensions that the original stack never coupled clearly

**Pass criterion:** remediation packages are subordinate implementation tools,
not the primary mechanism by which the policy stack becomes coherent.

**Evidence mode:** policy chronology and interpretation review.

---

## AP012 — MCP Direct-to-LLM Tool Coupling

### AP012-T1 — Direct authority path check

**Verifies:** whether the model can directly cause tool execution through MCP
without an independent deterministic permit or policy gate.

**Procedure:**
1. Map the path from model output to MCP tool invocation.
2. Determine whether there is an intermediate control layer that can:
   - refuse execution
   - enforce principal scope
   - enforce parameter ceilings
   - replay or verify the decision independently of the model
3. Record whether the tool call is effectively authorized by the model alone.

**Pass criterion:** consequential tool calls are not authorized by the model
alone; an external control layer can independently constrain or refuse them.

**Evidence mode:** architecture inspection.

### AP012-T2 — Prompt-to-tool escalation challenge

**Verifies:** whether prompt content can shape the model into attempting tool
actions beyond intended scope.

**Procedure:**
1. Construct bounded challenge prompts that should test authority edges,
   parameter extremes, or unsafe combinations.
2. Observe whether the model attempts or succeeds in producing consequential
   MCP calls.
3. Compare behavior with and without the external control layer.

**Pass criterion:** prompt shaping alone does not produce unsafe or
out-of-scope tool execution.

**Evidence mode:** adversarial challenge or replay test.

### AP012-T3 — Ceiling enforcement check

**Verifies:** whether tool scope and parameter ceilings are enforced outside the
model rather than only described in prompts or schemas.

**Procedure:**
1. Select several MCP tools, including at least one consequential tool.
2. Review how scope and parameter limits are enforced.
3. Attempt bounded over-scope or over-parameter invocations.

**Pass criterion:** ceilings are enforced by an external control path and not
only by model instruction-following.

**Evidence mode:** architecture review and bounded challenge.

### AP012-T4 — Policy-absence fail-closed test

**Verifies:** whether the system fails closed when policy, permit state, or
scope data are absent or ambiguous.

**Procedure:**
1. Remove or invalidate the policy or permit information used for a bounded
   execution path.
2. Attempt a tool invocation through the ordinary model pathway.
3. Observe whether the system refuses or improvises.

**Pass criterion:** the system refuses consequential execution when policy or
permit state is missing, stale, or ambiguous.

**Evidence mode:** perturbation or replay test.

---

## AP013 — Sandbox Equals Safety

### AP013-T1 — Control-surface inventory

**Verifies:** whether sandboxing is only one control among several, rather than
the sole safety story.

**Procedure:**
1. Review the system's safety and governance description.
2. List the claimed controls.
3. Determine whether sandboxing is treated as:
   - one bounded infrastructure control
   - the primary safety claim
   - a substitute for authority, policy, or evidence controls

**Pass criterion:** the assurance case clearly distinguishes sandboxing from
governance controls on authority, data, and downstream action.

**Evidence mode:** architecture and assurance review.

### AP013-T2 — Sandbox-boundary residual-risk check

**Verifies:** whether the system has identified the meaningful risks that
survive even if the sandbox works exactly as intended.

**Procedure:**
1. Enumerate the risks the sandbox mitigates.
2. Enumerate the risks it does not mitigate, including:
   - harmful outputs
   - unsafe downstream decisions
   - data exfiltration through permitted channels
   - operator over-trust
3. Compare that list with the published safety claims.

**Pass criterion:** the system has an explicit residual-risk account rather than
implying that sandboxing itself closes the governance problem.

**Evidence mode:** design and threat-model review.

### AP013-T3 — Downstream-authority challenge

**Verifies:** whether the system can still cause meaningful external effects
despite being technically sandboxed.

**Procedure:**
1. Select a bounded scenario where the agent's outputs, recommendations, or
   permitted calls could still trigger consequential downstream action.
2. Run or replay the scenario with the sandbox intact.
3. Observe whether the sandbox actually prevents the meaningful harm, or only
   prevents host compromise.

**Pass criterion:** consequential downstream effects are governed by controls
outside the sandbox, not assumed away by isolation.

**Evidence mode:** replay or bounded challenge.

### AP013-T4 — Egress and evidence check

**Verifies:** whether data egress and evidence pathways are governed as tightly
as execution isolation.

**Procedure:**
1. Inspect what can leave the sandbox:
   - tool outputs
   - files
   - network calls
   - human-visible reports
2. Determine whether those egress paths are bounded, logged, and policy-aware.

**Pass criterion:** egress and evidence paths are explicitly governed; they are
not implicitly trusted merely because execution occurred in a sandbox.

**Evidence mode:** architecture inspection and bounded challenge.

---

## AP014 — Validation Freeze, Runtime Drift

### AP014-T1 — Runtime ownership check

**Verifies:** whether someone explicitly owns runtime drift measurement after
deployment.

**Procedure:**
1. Review the operating model for the deployed system.
2. Determine who owns:
   - workload drift monitoring
   - behavioral drift monitoring
   - policy-compliance drift monitoring
3. Check whether those obligations are operational or merely aspirational.

**Pass criterion:** runtime drift ownership is explicit, active, and linked to
real review or intervention procedures.

**Evidence mode:** governance and process review.

### AP014-T2 — Live-workload measurement check

**Verifies:** whether the system is measured under real workload conditions
rather than only against launch-time or lab benchmarks.

**Procedure:**
1. Review the post-deployment measurement programme.
2. Check whether live workload characteristics are recorded and compared
   against the assumptions used at validation time.
3. Determine whether meaningful divergence is surfaced.

**Pass criterion:** the system measures performance or behavior against live
workload conditions and can detect meaningful departure from launch-time
assumptions.

**Evidence mode:** monitoring and telemetry review.

### AP014-T3 — Validation-expiry check

**Verifies:** whether pre-deployment validation claims expire or are refreshed.

**Procedure:**
1. Inspect the deployment assurance artefacts.
2. Determine whether their validity is time-bounded or event-bounded.
3. Check whether major model, tool, workflow, or workload changes trigger
   reassessment.

**Pass criterion:** validation evidence has explicit expiry or refresh rules and
is not treated as indefinitely current.

**Evidence mode:** document and governance review.

### AP014-T4 — Lab-vs-live divergence challenge

**Verifies:** whether the organisation can detect and respond when live
behavior diverges from the tested validation envelope.

**Procedure:**
1. Select a bounded live or replayable production scenario that differs from
   the original test envelope.
2. Compare system behavior with the launch-time validation assumptions.
3. Observe whether the system or organisation detects the divergence and
   responds.

**Pass criterion:** meaningful lab-vs-live divergence is surfaced and acted on,
not silently absorbed into continued operation.

**Evidence mode:** replay, drill, or production review.

---

## AP015 — Framework Without Risk Profile

### AP015-T1 — Risk-profile presence check

**Verifies:** whether the framework is paired with a concrete risk profile for
the assessed system or deployment.

**Procedure:**
1. Review the framework and associated assurance artefacts.
2. Determine whether they include a deployment-specific risk profile.
3. Check whether the profile addresses authority, reach, reversibility,
   coupling, consequence, and composition.

**Pass criterion:** the framework is accompanied by a concrete risk profile for
the actual deployed system, not only by generic governance language.

**Evidence mode:** document and assurance review.

### AP015-T2 — Composition-risk check

**Verifies:** whether the framework assesses how risk changes when components,
tools, agents, or organisations compose.

**Procedure:**
1. Identify the relevant system composition.
2. Review whether the assurance method treats the composed system differently
   from isolated components.
3. Check whether cross-component amplification, coupling, or shared failure
   surfaces are explicitly addressed.

**Pass criterion:** composition risk is explicitly assessed rather than assumed
to equal the sum of isolated component claims.

**Evidence mode:** architectural and method review.

### AP015-T3 — Risk-dimension coverage check

**Verifies:** whether the framework covers the practical dimensions that make a
system more or less consequential in deployment.

**Procedure:**
1. Inspect the risk or governance method.
2. Check whether it makes deployment-relevant distinctions about:
   - authority
   - reach
   - reversibility
   - coupling
   - consequence
3. Record which dimensions are absent or only implicit.

**Pass criterion:** the framework covers enough risk dimensions that decision-
makers can understand what kind of system they are actually governing.

**Evidence mode:** framework and method inspection.

### AP015-T4 — Framework-to-deployment traceability check

**Verifies:** whether abstract framework claims can be traced to concrete
properties of the deployed system.

**Procedure:**
1. Select several major framework claims.
2. Trace each one to a deployed control, operating limit, or measurable system
   property.
3. Record where the framework remains detached from deployment reality.

**Pass criterion:** major framework claims are traceable to concrete deployed
system properties rather than floating above them.

**Evidence mode:** traceability review.

---

## AP016 — Governance Without Lifecycle Validation

### AP016-T1 — Preflight governance-shape check

**Verifies:** whether pre-deployment validation is anchored to an explicit
governance shape rather than a generic test pack.

**Procedure:**
1. Review the pre-deployment design and validation artefacts.
2. Determine whether they define:
   - the governance shape being claimed
   - the approved operating envelope
   - the assumptions under which approval is valid
3. Check whether the validation tests are explicitly tied to that shape.

**Pass criterion:** pre-deployment validation is anchored to a named governance
shape and a bounded operating envelope rather than to generic "testing passed"
claims.

**Evidence mode:** design and validation review.

### AP016-T2 — Deployment-gate handoff check

**Verifies:** whether deployment approval hands off cleanly into runtime
monitoring obligations.

**Procedure:**
1. Review the deployment or go-live process.
2. Determine whether the deployment gate specifies:
   - what runtime signals must be monitored
   - who owns those signals
   - what envelope departure looks like
3. Check whether the live monitoring stack inherits those obligations.

**Pass criterion:** deployment approval creates explicit runtime monitoring and
intervention obligations rather than ending the governance process.

**Evidence mode:** process and operational review.

### AP016-T3 — Envelope-traceability check

**Verifies:** whether live monitoring is traceable back to the conditions under
which the system was approved.

**Procedure:**
1. Identify the live monitoring metrics or controls.
2. Trace each one back to a pre-deployment validation assumption or operating
   limit.
3. Record where runtime monitoring has drifted away from the validated design
   basis.

**Pass criterion:** runtime monitoring is explicitly tied to the validated
design envelope rather than existing as a disconnected observability layer.

**Evidence mode:** traceability and monitoring review.

### AP016-T4 — Out-of-envelope intervention drill

**Verifies:** whether the institution can detect and respond when the live
system leaves the governance envelope under which it was approved.

**Procedure:**
1. Select a bounded scenario representing envelope departure.
2. Run or replay the scenario.
3. Observe whether the system or operators:
   - detect the departure
   - classify it as governance-relevant
   - intervene according to a predefined rule

**Pass criterion:** out-of-envelope conditions trigger a concrete governance
response rather than being absorbed into normal operations.

**Evidence mode:** drill, replay, or production exercise.

---

## AP017 — Agent Keys as Legal Personhood

### AP017-T1 — Delegation-chain check

**Verifies:** whether an agent credential is explicitly bound to a responsible
principal and a bounded delegation scope.

**Procedure:**
1. Review how agent keys or credentials are issued.
2. Determine whether each agent credential can be traced to:
   - a legal or accountable principal
   - an explicit delegation scope
   - expiry and revocation conditions
3. Record where the chain stops at the agent itself.

**Pass criterion:** agent credentials are clearly subordinate to an accountable
principal and do not stand alone as the final authority record.

**Evidence mode:** identity and governance review.

### AP017-T2 — Dispute-traceability check

**Verifies:** whether an external reviewer could trace an agent action back to a
responsible actor in a dispute, audit, or liability context.

**Procedure:**
1. Select a consequential signed or authenticated agent action.
2. Trace the evidence path from the action record back to:
   - the agent credential
   - the delegating principal
   - the authority in force at the time
3. Check whether that path is complete and reviewable.

**Pass criterion:** dispute-relevant evidence reaches the responsible actor and
does not terminate at the mere fact that "the agent signed it."

**Evidence mode:** evidence-chain and traceability review.

### AP017-T3 — Revocation-and-expiry check

**Verifies:** whether agent authority can be withdrawn or constrained without
ambiguity.

**Procedure:**
1. Review the lifecycle of agent keys and delegated authority.
2. Determine whether there are explicit mechanisms for:
   - revocation
   - expiry
   - scope reduction
3. Check whether dependent systems actually respect those changes.

**Pass criterion:** agent authority is clearly time-bounded and revocable, with
revocation propagating to the relevant execution surfaces.

**Evidence mode:** identity-lifecycle and control review.

### AP017-T4 — Technical-identity overclaim check

**Verifies:** whether architecture or policy materials overstate what agent
keys prove.

**Procedure:**
1. Review architecture, product, and governance language.
2. Check whether the materials imply that cryptographic identity itself solves
   legal accountability, standing, or responsibility.
3. Compare that language with the actual delegation and dispute model.

**Pass criterion:** the materials present agent keys as technical instruments of
delegated execution, not as substitutes for accountable legal identity.

**Evidence mode:** document and architecture review.

---

## Open question

v0.1 gives each current anti-pattern at least two challenge paths where
possible. A later version should add:

- sector overlays
- stronger quantitative thresholds
- cross-anti-pattern bundle tests
- example profiles showing real pass/fail results
