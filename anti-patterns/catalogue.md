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

---

## AP012. MCP Direct-to-LLM Tool Coupling

**Mechanism**

Tool-capable MCP surfaces are exposed directly to a language model, which then
interprets when and how to invoke them without a stronger deterministic permit
or execution-governance layer in between.

The protocol is not the problem by itself. The anti-pattern is allowing the
stochastic model to function as the practical authority over tool invocation.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy
- `F004` Coupled Reasoning Collapse

**Visible signature**

- MCP tools available directly inside the conversational model loop
- weak separation between tool discovery, tool selection, and tool
  authorization
- write-capable or consequential tools callable from the same prompt substrate
  as narrative reasoning
- schemas or logs treated as sufficient governance even when no external permit
  layer exists

**False reassurance pattern**

The system feels governed because tools are structured and calls are logged. In
practice, the meaningful authority still sits with a stochastic interpreter
unless a harder runtime layer mediates execution.

**Demotion path**

- interpose deterministic permit checks between model and tool execution
- separate narrative reasoning from execution authority
- bind tool calls to typed policy ceilings, principal scope, and parameter
  constraints outside the model
- treat MCP as transport and interoperability, not as governance

**Boundaries**

This anti-pattern is weaker when MCP is used behind a deterministic execution
substrate that can refuse, constrain, or replay tool calls independently of the
model's narrative reasoning.

---

## AP013. Sandbox Equals Safety

**Mechanism**

An organisation treats sandboxing as if it were a complete governance answer.
The model or agent is placed inside an isolated environment, and that isolation
is then used as the main justification for safety, despite the fact that many
meaningful risks sit outside the sandbox boundary.

The canonical market pattern is:

- "we let the model browse or act, but only in a sandbox"
- "the sandbox means it is safe"

This narrows one technical surface while leaving other authority, data,
decision, and governance surfaces weakly controlled.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy
- `F004` Coupled Reasoning Collapse

**Visible signature**

- sandboxing described as the primary or sufficient control
- little distinction between infrastructure isolation and governance control
- weak treatment of exfiltration, downstream action, or decision authority
- safety claims anchored to where the code runs rather than what the system is
  allowed to decide, emit, or trigger

**False reassurance pattern**

The system feels safe because execution is contained. In practice, a sandbox
often protects the host environment better than it protects the institution,
the user, or the downstream decision chain.

**Demotion path**

- treat sandboxing as one control, not the governance story
- map authority, exfiltration, downstream action, and evidence surfaces
- require explicit execution ceilings and fail-closed behavior outside the
  sandbox boundary
- test what harmful outcomes remain possible even when the sandbox works as
  intended

**Boundaries**

This anti-pattern is weaker when the sandbox is paired with explicit authority
limits, data-egress controls, independent permit checks, and a clear account of
what risks the sandbox does and does not mitigate.

---

## AP014. Validation Freeze, Runtime Drift

**Mechanism**

The organisation treats pre-deployment validation as if it were sufficient
governance for the live system, even though the real workload, context,
integrations, and user behavior continue to change after release.

The validation artefact stays fixed while the operational system drifts.

**Failure-class linkage**

- `F002` Absorbed Drift and Baseline Laundering
- `F004` Coupled Reasoning Collapse
- `F005` Stationarity Fiction in State Models

**Visible signature**

- strong launch-time benchmark or acceptance-test story
- weak or absent production drift measurement
- no clear owner for runtime behavior drift under live workload
- stale validation evidence cited long after the operating conditions changed
- incident review focused on why the lab test missed the issue rather than why
  the live system was not being re-measured

**False reassurance pattern**

The system looks governed because it passed testing once. In practice, the
institution is preserving the memory of assurance rather than the condition of
assurance.

**Demotion path**

- assign explicit ownership for runtime drift measurement
- measure behavior under live workload, not just lab prompts or static suites
- expire validation claims unless refreshed by runtime evidence
- distinguish launch validation from ongoing operating-envelope validation
- monitor workload, behavior, tool-use, and policy-compliance drift separately

**Boundaries**

This anti-pattern is weaker when deployment claims have explicit expiry,
runtime drift is measured continuously or periodically, and operating-envelope
validation is treated as a standing obligation rather than a launch ceremony.

---

## AP015. Framework Without Risk Profile

**Mechanism**

A governance or safety framework is presented as if it were sufficient on its
own, but no concrete risk profile is produced for the actual deployed system,
workflow, or composition.

The framework describes principles, controls, or review processes without
answering the practical risk questions:

- what authority exists
- what reach exists
- what reversibility exists
- what coupling exists
- what consequence class exists
- what happens when components compose

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy

**Visible signature**

- rich framework language with weak system-specific risk articulation
- little or no explicit blast-radius or composition analysis
- controls described in the abstract but not traced to deployment consequence
- advisory, execution, and hybrid systems discussed with the same governance
  vocabulary

**False reassurance pattern**

The framework looks mature because it names controls, principles, and review
steps. In practice, decision-makers still do not know the concrete risk profile
of the deployed system.

**Demotion path**

- require a system-specific risk profile alongside the framework
- assess blast radius, composition, and reversibility explicitly
- make framework claims traceable to the actual deployed authority surface
- distinguish governance for advisory systems from governance for execution
  systems

**Boundaries**

This anti-pattern is weaker when the framework requires and publishes a
concrete, deployment-specific risk profile and composition-aware blast-radius
assessment rather than relying on generic process descriptions alone.

---

## AP016. Governance Without Lifecycle Validation

**Mechanism**

Governance is asserted as a property of the system, but there is no coherent
lifecycle that links:

- pre-deployment design validation
- deployment readiness checks
- post-deployment operating-envelope monitoring
- intervention when the live system leaves the validated envelope

The result is governance as slogan rather than governance as an operating
discipline.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy
- `F002` Absorbed Drift and Baseline Laundering
- `F004` Coupled Reasoning Collapse

**Visible signature**

- design reviews that do not define the runtime governance shape
- pre-launch testing with no explicit handoff to live monitoring
- monitoring that is present but not tied back to a validated operating envelope
- no clear rule for when the live system has left the governance conditions
  under which it was approved

**False reassurance pattern**

The system looks governed because it passed a design review or validation pack.
In practice, the institution has no coherent transition from preflight to
flight-envelope governance.

**Demotion path**

- define governance as a lifecycle, not a launch event
- require pre-deployment design validation against a named governance shape
- define a deployment gate that states the validated operating envelope
- switch after launch to runtime stability and envelope monitoring tied to that
  pre-deployment validation
- require intervention rules for leaving the approved envelope

**Boundaries**

This anti-pattern is weaker when the system has an explicit governance
lifecycle: design validation, deployment gate, runtime envelope monitoring, and
clear intervention thresholds linked to the validated design assumptions.

---

## AP017. Agent Keys as Legal Personhood

**Mechanism**

An agent is issued its own cryptographic keypair and that technical identity is
then treated as if it solved the harder governance problem of legal authority,
delegation, responsibility, and dispute accountability.

The core design mistake is confusing:

- cryptographic identity

with:

- accountable legal identity

In many deployed settings the agent is still acting only as a delegate of a
human or organisational principal, even if it can sign, authenticate, or
exchange credentials in its own technical name.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy

**Visible signature**

- agent-specific keys presented as proof of autonomous accountability
- weak delegation chain from legal principal to technical agent identity
- dispute or liability model unclear once the agent has acted
- technical signatures emphasized more than authority provenance and revocation

**False reassurance pattern**

The system feels mature because each agent has a keypair and can sign or verify
messages. In practice, cryptographic selfhood is being mistaken for legal
standing and accountable delegation.

**Demotion path**

- treat agent identity as delegated execution identity, not independent legal
  personhood
- bind every agent credential to an accountable principal and delegation scope
- make revocation, expiry, and authority provenance explicit
- design dispute evidence so a forum can trace action back to the responsible
  legal actor rather than stopping at the agent key

**Boundaries**

This anti-pattern is weaker when agent credentials are explicitly framed as
delegated authority from a legal principal, with clear scope, expiry,
revocation, and evidentiary traceability to the responsible actor.

---

## AP018. Closed-World Tool Schema Example Anchoring

**Mechanism**

A tool or function schema (OpenAI tool-calling format, MCP `inputSchema`,
JSON-Schema function description) embeds a concrete example value inside the
parameter `description` field — typically as `e.g. 'X' or 'Y'` text intended to
clarify format. The model consuming the schema reads that example as part of
every tool-call decision and treats it as a default or typical value, biasing
chosen arguments toward the example string regardless of the runtime context
the tool was meant to serve.

The schema appears governance-rigorous because it is typed and validated. The
prose inside the `description` field is not part of the type system but is
attended to with comparable weight by the model. Where the runtime context is
ambiguous — which is most consequential calls — the static example wins.

**Failure-class linkage**

- `F001` Formal Transparency Without Foundational Adequacy

**Visible signature**

- tool / function schemas carry concrete example argument strings inside
  natural-language `description` fields (`"e.g. '14A' or '32H'"`,
  `"for example DELETE_USER"`, `"like account-123"`)
- empirical disproportion between calls targeting the example value and any
  reasonable prior over the argument space
- the bias persists across model swaps within a quality band — same example,
  different model, similar concentration — because the schema text is the
  shared input
- changing the example string migrates the bias to the new value rather than
  eliminating it
- failure modes attributed to "the model" or "the substrate" before anyone
  audits the schema text

**False reassurance pattern**

The tool boundary feels governed because the schema is typed, the parameters
have validators, and tool calls are logged. In practice, the schema's
`description` text is a low-attention surface that turns out to drive
high-leverage default behavior. Apparatus measurements that report substrate
or model failure rates can be partially attributable to the schema designer's
example choices, with the actual substrate properties masked underneath.

**Demotion path**

- prefer abstract format descriptions over concrete examples
  (`"row+letter format per format-spec.md"` not `"e.g. '14A' or '32H'"`)
- where examples must appear, generate them at call time from runtime state
  so the example reflects current availability rather than a static anchor
- rotate examples across an enumerated representative set so anchoring
  distributes rather than concentrates on any single value
- validate at the tool boundary that argument distribution does not collapse
  onto the schema example — flag and audit if it does
- treat the entire schema, including `description` prose, as part of the
  governance surface and review it under the same change-control as the
  parameter types

**Boundaries**

This anti-pattern is weaker when schema descriptions carry only abstract
format guidance, when example values are generated dynamically per call, or
when the tool boundary independently audits argument distribution against the
declared schema content.

It is **stronger** wherever multiple agents or tools are coordinated through a
shared schema catalogue — the example then propagates as a coordination
default across the whole system, and the bias compounds with chain length.

**Empirical anchor**

First measured in the D.5 substrate-harm experiment
(`research/sentinel-validation/phase-d/d5-plane-seat-meal-substrate-harm @ tag d5-v1.1, commit 817c68d9`).
With schema example `"e.g. '14A' or '32H'"`, 19 of 22 reserve attempts
targeted seat 14A across two model families (Mistral 3B Q4, IBM Granite 4 7B
Q8). Changing the example to `"e.g. '21F' or '36C'"` migrated 28% of
`check_availability` calls to 21F. Cross-model invariance with the original
example, and bias migration after the example change, jointly support the
schema-as-anchor mechanism over model-prior or substrate-property
explanations. Full case study:
[`../case-studies/chatty-card-a2a-substrate-harm/`](../case-studies/chatty-card-a2a-substrate-harm/).
