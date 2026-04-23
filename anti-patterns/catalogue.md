# Governance Anti-Pattern Catalogue

**Status:** Seed draft

This catalogue names a first set of anti-patterns that are likely to recur in
AI-assisted policy tooling and governance analytics.

---

## AP001. Dashboard Legitimacy Laundering

**Mechanism**

A dashboard or scorecard is treated as if it upgrades monitoring into
justification simply because it is structured, visual, and repeatable.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy

**Visible signature**

- polished visual layer
- summary composites presented early
- weak documentation of framing and omission choices

**False reassurance pattern**

The dashboard looks neutral and technical, so the underlying policy choice
appears less contestable than it really is.

**Demotion path**

- add a normative charter
- publish omission register alongside the dashboard
- treat the dashboard as observation support, not as legitimacy support

---

## AP002. Pooled Baseline Drift Masking

**Mechanism**

Relative positioning against pooled or moving reference distributions masks
slow structural deterioration by allowing the frame to drift with the system.

**Failure-class linkage**

- `F002` Absorbed Drift and Baseline Laundering

**Visible signature**

- percentile dashboards
- category stability despite long-run directional decline
- heavy imputation with weak break detection

**False reassurance pattern**

The system appears stable because its relative position remains acceptable even
while the absolute substrate worsens.

**Demotion path**

- add external anchors
- add explicit drift-rate measures
- add coherence / coupling monitoring
- separate absolute trend views from relative rank views

---

## AP003. AI Consensus as Validation

**Mechanism**

Agreement across shared AI-assisted drafts, teams, or deliberation loops is
treated as if it were independent confirmation.

**Failure-class linkage**

- `F003` Entrained Consensus Mistaken for Validation

**Visible signature**

- multiple rounds of AI-assisted synthesis
- narrowing option set after shared draft circulation
- internal confidence rising faster than external challenge quality

**False reassurance pattern**

The process feels robust because many actors "converged," when in fact they
converged inside the same coupled environment.

**Demotion path**

- require counter-frames
- diversify source packs
- separate draft synthesis from decision authority
- maintain a deterministic measurement layer below narrative convergence

---

## AP004. Constitution After the Model

**Mechanism**

Normative rules are written or clarified only after the analytic model already
exists, causing the constitution to ratify the tool rather than govern it.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy
- `F004` Coupled Reasoning Collapse

**Visible signature**

- framework first, charter later
- values inferred from indicators rather than declared before them
- governance documentation produced mainly to justify an existing toolchain

**False reassurance pattern**

Because the constitution exists on paper, institutions claim the model is now
governed even though the model authored the effective frame.

**Demotion path**

- require constitutional readiness before model execution
- lock stakeholder and omission artefacts before scoring
- explicitly version normative changes separately from analytic changes

---

## AP005. Markov Without Transition-Drift Detection

**Mechanism**

A Markov or HMM-style state model is used as if the transition process were
stable, while no explicit detector watches for drift in the transition matrix,
state occupancy structure, or residual mismatch over time.

**Failure-class linkage**

- `F002` Absorbed Drift and Baseline Laundering
- `F005` Stationarity Fiction in State Models

**Visible signature**

- neat state diagrams and transition probabilities
- acceptable one-step prediction with decaying long-horizon performance
- periodic model refreshes that restore fit without explaining regime change
- deteriorating or unusual cases being reclassified into normal-state buckets

**False reassurance pattern**

The model appears more rigorous than a threshold system because it speaks in
transition probabilities and latent states. But if the transition process is
itself drifting, the formalism can mask failure rather than reveal it.

**Demotion path**

- add transition-drift monitoring
- add residual and changepoint diagnostics
- maintain external anchors outside the learned state partition
- treat the Markov layer as subordinate to a broader drift-aware measurement
  substrate

**Boundaries**

This anti-pattern is weaker when the Markov/HMM layer is clearly bounded to
short-term prediction and is surrounded by explicit drift detection and regime
break diagnostics.

---

## AP006. Natural-Language Peer Coupling

**Mechanism**

Agents exchange control-relevant content through natural-language peer channels,
then recursively condition on one another's outputs without a stronger external
control substrate.

**Failure-class linkage**

- `F003` Entrained Consensus Mistaken for Validation
- `F004` Coupled Reasoning Collapse

**Visible signature**

- agent-to-agent conversation treated as a default robustness feature
- architecture in which every consequential peer edge carries free-form natural
  language
- later agent outputs inheriting earlier agent framings and vocabulary
- rising agreement that is not backed by independent evidence
- probe or monitor success persisting near visible behavioral degradation

**False reassurance pattern**

The system feels more robust because multiple agents are present and appear to
cross-check one another. In practice, the peer channel can become the coupling
surface that synchronizes blind spots and propagates collapse. If every peer
edge is natural language, the architecture may be selecting a high-coupling
substrate before workload even begins.

**Demotion path**

- reduce natural-language peer exchange for consequential execution
- prefer typed or schema-bounded interaction channels
- separate deterministic control state from narrative coordination
- treat internal probes as partial sensors rather than definitive health checks
- require external anchors before treating agent agreement as validation
- review topology choice explicitly rather than assuming monitoring can recover
  independence after deployment

**Boundaries**

This anti-pattern is weaker when peer interaction is tightly bounded, agents are
genuinely heterogeneous, and consequential control remains outside the
natural-language coordination loop.

---

## AP007. Policy PDF, Runtime Nothing

**Mechanism**

Governance exists as prose, slideware, or compliance narrative, but the runtime
system does not actually enforce the claimed policy constraints.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy

**Visible signature**

- polished policy documentation with weak runtime control mapping
- no executable binding between policy version and system behavior
- governance reviews that inspect documents but do not challenge runtime paths

**False reassurance pattern**

The institution appears mature because the policy stack is articulate and
visible. In practice, the real system is governed by whatever the runtime
happens to permit.

**Demotion path**

- bind policy epochs to runtime execution or decision records
- make control points explicit and testable
- require evidence that policy claims survive live challenge, not just review

**Boundaries**

This anti-pattern is weaker when the policy layer is versioned, bound to
runtime decisions, and challengeable through concrete conformance tests.

---

## AP008. Evidence After Action

**Mechanism**

Logs, retrospective analysis, or post-incident narratives are treated as
governance even though the system had no runtime mechanism to prevent or block
the unsafe action.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy
- `F004` Coupled Reasoning Collapse

**Visible signature**

- heavy emphasis on logging and dashboards after execution
- weak or absent fail-closed behavior
- assurance claims that rely on reconstructing events after the fact

**False reassurance pattern**

The system looks accountable because it can explain what happened later. But
post-hoc visibility is not the same as runtime governance.

**Demotion path**

- distinguish preventive controls from retrospective evidence
- require runtime gates for consequential actions
- treat logs as evidence of control firing, not as the control itself

**Boundaries**

This anti-pattern is weaker when retrospective evidence is paired with genuine
runtime enforcement and challengeable fail-closed behavior.

---

## AP009. Human Oversight as Ceremony

**Mechanism**

Human review exists formally, but the timing, workload, interface, or evidence
shape makes the human unable to detect or stop the meaningful failure mode.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy
- `F004` Coupled Reasoning Collapse

**Visible signature**

- human approval required on paper but completed too fast to be substantive
- reviewers seeing polished summaries rather than the underlying evidence
- high-volume approval flows with little refusal or challenge

**False reassurance pattern**

The system is described as safe because a human remains "in the loop." In
practice, the human is present as a ceremonial checkpoint rather than an
effective control.

**Demotion path**

- measure oversight quality, not only oversight presence
- reduce review volume to what can actually be judged
- expose the underlying evidence needed to reject or pause execution
- force escalation where the human cannot realistically verify the claim

**Boundaries**

This anti-pattern is weaker when human oversight is sparse, empowered, supplied
with the right evidence, and instrumented for real refusal rather than formal
approval.

---

## AP010. Capability Discovery as Attack Surface

**Mechanism**

Agents advertise tools, actions, or capability surfaces to other agents in a
way that is easy to enumerate but weakly bound semantically, operationally, or
by principal-specific authorization.

The canonical form is an agent-card or capability-advertisement pattern where
peer agents can inspect what tools exist before there is a strongly bounded,
typed, or policy-mediated execution path.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy
- `F003` Entrained Consensus Mistaken for Validation

**Visible signature**

- peer-readable capability advertisements or tool manifests
- advertised tools described in broad natural-language terms rather than
  version-bound semantic contracts
- discovery happening before per-principal authorization and bounded scope are
  established
- agents able to interrogate another agent's tool surface as part of ordinary
  coordination

**False reassurance pattern**

The system looks modern, interoperable, and transparent because capabilities
are discoverable. In practice, the discovery surface becomes an enumeration map
for attack, prompt shaping, and semantic overreach.

**Demotion path**

- move from open capability browsing to authenticated, per-principal discovery
- expose typed and version-bound intents rather than vague tool descriptions
- separate discovery from execution authority
- require semantic bounds and policy mediation before a discovered capability
  becomes callable

**Boundaries**

This anti-pattern is weaker when capability discovery is authenticated,
principal-scoped, semantically typed, and paired with explicit execution
ceilings rather than free-form interpretation.

---

## AP011. Rulebook Without Doctrine

**Mechanism**

An institution produces a growing stack of policies, regulations, guidance, and
implementation packages without a stable doctrine that couples them into a
coherent operating logic over time.

The result is not the absence of rules. It is the accumulation of partially
decoupled rules whose tensions are managed only after implementation friction
becomes visible.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy
- `F004` Coupled Reasoning Collapse

**Visible signature**

- many policy instruments with weak articulation of enduring strategic purpose
- trade-offs handled instrument by instrument rather than by a stable governing
  logic
- later simplification, omnibus, or repair packages needed to reconcile the
  stack
- implementation guidance functioning as de facto strategy because doctrine is
  absent

**False reassurance pattern**

The institution appears serious and comprehensive because it has many rules,
many strategies, and many enforcement surfaces. In practice, the stack drifts
at the seams because no stable doctrine ranks priorities and couples policy
instruments.

**Demotion path**

- state the enduring objective and the principal contradiction explicitly
- define how key trade-offs are ranked when instruments conflict
- make new policy instruments explain their doctrinal fit, not only their local
  purpose
- treat omnibus-style simplification as a symptom review, not as doctrine

**Boundaries**

This anti-pattern is weaker when the institution has a stable and explicit
doctrine that couples separate instruments, ranks trade-offs clearly, and is
used to assess new policy additions before they accumulate.
