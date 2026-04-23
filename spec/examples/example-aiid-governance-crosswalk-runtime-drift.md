# Example Crosswalk — Runtime Drift Interpretation

## Source stub

- Source system: AI Incident Database
- Record type: illustrative post-deployment case
- Public signal: system passed testing, harmful behavior emerged later under
  live workload, monitoring lag is visible

## Observed outcome

The public incident record suggests a system that had an acceptable pre-release
story but later behaved harmfully under live conditions not adequately caught by
the operating governance layer.

## Governance interpretation

The strongest governance reading is not simply “the model failed.”

It is:

- the validation story appears to have remained in force after the operating
  conditions changed
- runtime evidence and ownership look weaker than the deployment claim
- the governance layer may have become descriptive rather than controlling

## Candidate failure classes

- `F009` Validation-Lifecycle Break
- `F007` Runtime Governance Substitution

## Candidate anti-patterns

- `AP014` Validation Freeze, Runtime Drift
- `AP008` Evidence After Action

## Candidate constructive patterns

- `governance lifecycle validation`
- `runtime evidence`
- `coherence monitoring`

## Candidate mitigations

- define a runtime owner for drift and operating-envelope departure
- expire stale validation claims rather than letting them persist indefinitely
- bind live monitoring explicitly to the conditions validated at launch

## Confidence

`medium`

The incident supports a strong lifecycle interpretation, but the public record
may not fully expose the internal monitoring and intervention design.
