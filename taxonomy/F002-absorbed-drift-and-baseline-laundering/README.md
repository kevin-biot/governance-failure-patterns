# F002 — Absorbed Drift and Baseline Laundering

## Claim

Slow deterioration can be normalized by the monitoring frame itself, causing a
system to treat decline as the new normal.

## Mechanism

The baseline moves with the deteriorating system. Relative stability is then
mistaken for actual health.

## Observable Signature

- weak long-horizon alerts despite clear secular change
- category stability masking directional decline
- systems that notice shocks but not slow degradation

## False Reassurance Pattern

The monitoring surface reports normality because the reference class has
drifted with the target.

## Minimal Assumptions

- the monitoring system relies heavily on relative comparison
- baseline updates are automatic or weakly governed
- long-term external anchors are absent or underused

## Where It Does Not Apply

This class is weaker when strong external reference anchors are maintained and
drift rate is tracked explicitly.

## Mitigations

- external reference anchor
- explicit drift-rate computation
- absorbed-drift tests
- coherence monitoring alongside level monitoring
