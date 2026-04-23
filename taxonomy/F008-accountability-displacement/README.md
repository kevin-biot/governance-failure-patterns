# F008 — Accountability Displacement

## Claim

A system can displace accountability from the responsible principal onto
technical proxies such as agent credentials, registration status, or trace
artifacts, making the accountable actor harder rather than easier to identify.

## Mechanism

The failure appears when:

- technical identity is treated as if it created accountable standing
- registration or traceability is treated as if it resolved delegation
- dispute evidence stops at the technical actor rather than the legal actor

## Observable Signature

- strong emphasis on registration, traceability, or agent keys
- weak delegation chain to a responsible principal
- unclear liability or dispute model once the agent has acted

## False Reassurance Pattern

The system feels more accountable because it can identify the technical actor.
In practice, accountability has been displaced away from the party that remains
legally or operationally responsible.

## Minimal Assumptions

- agents or technical proxies can act consequentially
- a responsible principal still exists behind them
- the evidence model can stop at the proxy rather than the principal

## Where It Does Not Apply

This class is weaker when delegation, revocation, expiry, and dispute
traceability to the principal are explicit.

## Typical Cases

- agent keys treated as legal personhood
- registered agents treated as if registration itself solved accountability

## Mitigations

- use delegated identity models
- trace every consequential action back to a responsible principal
- make revocation and scope explicit

## Residual Risk

Even with delegated identity, complex multi-party disputes remain hard. The
goal is not perfect blame assignment but accountable traceability.
