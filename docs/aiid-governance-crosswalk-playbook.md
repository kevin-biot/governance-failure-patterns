# AIID Governance Crosswalk — Playbook

## Purpose

This playbook turns the crosswalk method into an analyst workflow.

It is for the situation where someone has:

- an AI Incident Database record
- its applied taxonomy labels
- and a need to derive a careful governance interpretation without
  over-claiming

## Working principle

The goal is not to explain the entire incident.

The goal is to answer a narrower question:

> what governance failure pattern, if any, is plausibly visible in the public
> incident record, and what tightening path does that suggest?

## Analyst workflow

### 1. Capture the incident cleanly

Record:

- incident id
- title
- source URL
- relevant source taxonomy labels
- a short observed-outcome summary

Do not begin with governance theory yet.

### 2. Extract the visible governance cues

Look for signals such as:

- pre-deployment testing mentioned
- post-deployment drift or surprise
- missing runtime controls
- registration or traceability language
- policy or oversight language
- refusal, override, or exception behavior
- evidence or logging claims
- migration, portability, or cross-system effects

These cues are more useful than generic incident description alone.

### 3. Ask the first governance question

Which of these seems most plausible?

- governance existed only on paper
- governance existed at launch but broke at runtime
- governance existed technically but displaced accountability
- governance language was stronger than risk profiling
- control was claimed, but evidence or refusal semantics were weak

This step narrows the search space.

### 4. Map to failure classes

Prefer the deeper mechanism before the visible anti-pattern.

Examples:

- stale validation story -> `F009`
- post-hoc logging as governance -> `F007`
- technical registration treated as accountability -> `F008`
- no deployment-specific risk framing -> `F010`

### 5. Map to anti-patterns

Then ask which deployer-visible habit fits best.

Examples:

- `AP014` Validation Freeze, Runtime Drift
- `AP008` Evidence After Action
- `AP017` Agent Keys as Legal Personhood
- `AP015` Framework Without Risk Profile

### 6. Add constructive patterns

Do not stop at diagnosis.

Add:

- candidate patterns
- candidate mitigations
- any key uncertainty about fit

This is what makes the crosswalk useful rather than merely critical.

### 7. Score confidence

Use:

- `high`
- `medium`
- `low`

Confidence should reflect the evidence for the governance interpretation, not
the severity of the incident.

## Common analyst errors

### Error 1: forcing one incident into one anti-pattern

Many incidents support multiple plausible governance readings.

### Error 2: treating harm category as governance category

An incident domain like misinformation or fraud does not tell you the governance
failure by itself.

### Error 3: overstating causality

Public incident records often show outcomes more clearly than internal control
design.

### Error 4: skipping mitigation

A crosswalk that ends at naming failure is less useful than one that points to
what should be tightened.

## Suggested output format

For each mapped incident, produce:

- one-paragraph observed outcome
- one-paragraph governance interpretation
- mapped failure classes
- mapped anti-patterns
- mapped constructive patterns
- mitigation list
- confidence and ambiguity notes

## Good use cases

- creating a pilot corpus of governance-tagged AI incidents
- testing whether the taxonomy is practically useful
- comparing incident-side labels with governance-side labels
- identifying recurrent mitigation gaps across incident clusters

## Boundaries

This playbook is not a substitute for incident investigation.

It is a structured overlay for governance interpretation using public records.
