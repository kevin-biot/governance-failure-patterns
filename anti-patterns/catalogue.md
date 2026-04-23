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
- later agent outputs inheriting earlier agent framings and vocabulary
- rising agreement that is not backed by independent evidence
- probe or monitor success persisting near visible behavioral degradation

**False reassurance pattern**

The system feels more robust because multiple agents are present and appear to
cross-check one another. In practice, the peer channel can become the coupling
surface that synchronizes blind spots and propagates collapse.

**Demotion path**

- reduce natural-language peer exchange for consequential execution
- prefer typed or schema-bounded interaction channels
- separate deterministic control state from narrative coordination
- treat internal probes as partial sensors rather than definitive health checks
- require external anchors before treating agent agreement as validation

**Boundaries**

This anti-pattern is weaker when peer interaction is tightly bounded, agents are
genuinely heterogeneous, and consequential control remains outside the
natural-language coordination loop.
