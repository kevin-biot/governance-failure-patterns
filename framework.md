# Framework

## What This Repository Calls a Governance Failure Pattern

A governance failure pattern is a recurrent way in which a decision-support
system, policy-analysis stack, or AI-assisted institutional workflow becomes
more fragile, less accountable, or less valid than it appears.

The emphasis is on **classes**, not anecdotes.

## Why a Pattern Taxonomy

Individual critiques are easy to dismiss as:

- one-off disagreement
- institutional politics
- implementation detail
- academic nitpicking

Pattern language changes that. A named class lets different cases be compared
without claiming they are identical.

## Repository Model

Each failure class should have the same spine:

- claim
- mechanism
- observable signature
- false reassurance pattern
- enabling assumptions
- boundaries of applicability
- mitigations
- residual risk

Each case study should answer:

- which class is present
- what evidence suggests it
- what is inference versus source-backed fact
- what tightening path is available

Each anti-pattern should answer:

- what the bad habit or design move is called
- how it amplifies one or more failure classes
- what visible symptoms it produces in practice
- what demotion or remediation path would reduce the damage

## Design Principle

This repository is not anti-tool and not anti-institution by default.

Its stance is:

- critique weak governance honestly
- identify where fragility is structural
- pair criticism with bounded repair patterns where possible

## Failure Classes vs Anti-Patterns

The repository distinguishes between:

- **failure classes** — deeper recurrent mechanisms of fragility
- **anti-patterns** — recognizable deployer-visible habits, architectures, or
  workflow choices that instantiate or amplify those mechanisms

This distinction matters because public dialogue often begins with visible bad
practice rather than with abstract mechanism. Anti-patterns are therefore the
operational front-end of the taxonomy.

## Three Layers

The current working model distinguishes three broad layers:

### Layer 1 — Normative Governance

Who counts, what values govern, which harms are non-compensable, and which time
horizons matter.

### Layer 2 — Analytic / Measurement Substrate

The explicit transforms, indicators, models, and state estimates used to detect
change, compare options, or structure decisions.

### Layer 3 — Explanatory / Deliberative Layer

Narrative explanation, stakeholder interpretation, human-AI framing loops, and
other meaning-making processes above the measurement layer.

Many failures happen because institutions confuse these layers or let one
silently substitute for another.
