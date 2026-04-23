# F009 — Validation-Lifecycle Break

## Claim

Governance fails when pre-deployment validation, deployment approval, and
runtime monitoring are treated as disconnected activities rather than as one
continuous operating discipline.

## Mechanism

The failure emerges when:

- design validation is not tied to a named governance shape
- deployment approval does not hand off to runtime obligations
- live monitoring is not traced back to the approved envelope
- stale validation evidence continues to stand in for current assurance

## Observable Signature

- testing passed once, governance assumed thereafter
- no explicit runtime drift owner
- no envelope-departure rule linked to launch assumptions
- live monitoring disconnected from design-basis validation

## False Reassurance Pattern

The system looks governed because there was a strong launch validation event.
In practice, the live system has drifted away from the conditions under which
it was approved.

## Minimal Assumptions

- the system changes under live workload or context
- governance claims were established before deployment
- no strong lifecycle handoff exists

## Where It Does Not Apply

This class is weaker when the system has explicit preflight validation,
deployment gates, runtime envelope monitoring, and intervention rules linked
end-to-end.

## Typical Cases

- validation freeze, runtime drift
- governance without lifecycle validation

## Mitigations

- define a governance lifecycle
- time-bound or event-bound validation claims
- monitor against the approved operating envelope

## Residual Risk

Even a good lifecycle model will miss some novel conditions. The gain is
continuity of governance, not omniscience.
