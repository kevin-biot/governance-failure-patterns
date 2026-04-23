# OECD Catalogue to Governance Failure Patterns — Crosswalk Method

## Purpose

This note defines a bounded method for using the OECD Catalogue of Tools &
Metrics for Trustworthy AI as a mitigation-side crosswalk for this repository.

The point is not to treat the OECD catalogue as an endorsement list or as a
proof that a governance problem is solved.

The point is to use it as a structured public source of:

- technical tools
- procedural tools
- educational tools
- metrics and benchmarks

that may help mitigate some governance failure patterns.

## Source relationship

The OECD catalogue is best understood as a public inventory of tools and
metrics intended to support trustworthy AI implementation.

Useful public source pages include:

- [Catalogue overview](https://oecd.ai/en/catalogue/overview)
- [About the catalogue / FAQ](https://oecd.ai/en/catalogue/faq)

From those public materials, the catalogue:

- aims to help AI actors find tools and metrics for trustworthy AI
- includes technical, procedural, and educational tools
- allows open submission and use-case sharing
- is not a formal endorsement or certification regime

## Core rule

The OECD crosswalk is a mitigation-supply overlay, not a governance verdict.

It must not imply:

- that a listed tool is endorsed by OECD as effective
- that tool availability means a governance failure is solved
- that every governance problem is reducible to a tooling gap

The correct use is narrower:

- identify public mitigation families
- connect them to anti-patterns or constructive patterns
- identify where tools are abundant
- identify where governance design still outruns tool supply

## What the OECD source says directly

The public catalogue and FAQ support these points directly:

- the catalogue exists to help users find tools and metrics for trustworthy AI
- tools are grouped into technical, procedural, and educational categories
- tools, metrics, and use cases can be submitted to the catalogue
- OECD does not endorse the listed tools or take responsibility for third-party
  issues

## What this repository infers

This repository adds the following interpretation:

- the catalogue can be used as a mitigation-side source for governance failure
  patterns
- some governance weaknesses are likely to have richer public tool support than
  others
- some governance weaknesses will remain thinly served because they are mainly
  institutional-design problems rather than tool problems

## Recommended record shape

Each OECD crosswalk record should include:

- `source_category`
- `source_url`
- `tool_or_metric_name`
- `catalogue_type`
- `candidate_failure_classes`
- `candidate_anti_patterns`
- `candidate_patterns`
- `candidate_mitigation_role`
- `fit_confidence`
- `limitations`

## Mapping steps

### 1. Start with the governance problem

Begin with:

- a failure class
- an anti-pattern
- or a constructive pattern

Then ask whether the OECD catalogue appears to contain public tool categories
or methods that plausibly help.

### 2. Distinguish tool type

Keep the OECD tool type explicit:

- technical
- procedural
- educational
- metric

This matters because some anti-patterns are not mainly technical problems.

### 3. Record mitigation role, not just name

Ask what the tool or method would actually do:

- detect
- constrain
- document
- train
- benchmark
- audit
- support review

This is more useful than listing tool names alone.

### 4. Record limitations honestly

For every OECD-linked mitigation, ask:

- does this help detect the failure?
- prevent it?
- document it after the fact?
- only partially address it?

### 5. Identify supply gaps

Where the OECD catalogue is thin, record that explicitly.

This may be one of the most important outputs.

## Strong likely fit areas

The OECD catalogue is likely to be strongest where governance concerns overlap
with:

- fairness and bias measurement
- transparency and documentation tools
- robustness and security tools
- evaluation metrics and benchmarks
- procedural auditing guidance
- awareness and educational tooling

These are promising crosswalk areas for:

- `AP008` Evidence After Action
- `AP014` Validation Freeze, Runtime Drift
- selected transparency, documentation, or audit-related weaknesses

## Weak likely fit areas

The OECD catalogue is likely to be weaker where the central issue is:

- delegated accountability
- legal principal binding
- policy as runtime authority
- dispute-grade evidence
- portability governance
- doctrine-level policy coupling
- upstream constitutional framing

These are useful gap findings rather than failures of the catalogue.

## Example mapping shapes

### Example 1: Runtime drift problem

Governance target:

- `AP014` Validation Freeze, Runtime Drift

Likely OECD mitigation-side fit:

- monitoring metrics
- evaluation benchmarks
- procedural review methods

Expected limitation:

- tools may help detect or monitor drift
- but lifecycle ownership and intervention design remain institutional tasks

### Example 2: Accountability displacement problem

Governance target:

- `AP017` Agent Keys as Legal Personhood

Likely OECD mitigation-side fit:

- weak or indirect

Expected limitation:

- catalogue tools may support documentation or governance procedure
- but principal binding, revocation, and dispute accountability are not mainly
  tool problems

### Example 3: Policy-on-paper problem

Governance target:

- `AP007` Policy PDF, Runtime Nothing

Likely OECD mitigation-side fit:

- procedural governance tools
- documentation tools
- auditing methods

Expected limitation:

- these may improve process visibility
- but runtime binding still requires architectural control points, not just
  better documentation

## Boundaries

This crosswalk should remain disciplined.

It is useful only if it stays clear about three things:

- what OECD publishes directly
- what this repository infers about governance fit
- where tools are not enough and governance design is still the missing layer
