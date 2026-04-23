# F007 — Runtime Governance Substitution

## Claim

An institution can appear to govern a live system while substituting prose,
logs, dashboards, or ceremonial oversight for actual runtime control.

## Mechanism

The failure appears when:

- governance is described but not bound to execution
- retrospective evidence is mistaken for preventive control
- human oversight is present formally but ineffective in practice

## Observable Signature

- policy documents with weak runtime bindings
- logging and dashboards emphasized more than fail-closed controls
- oversight present on paper but unable to stop the meaningful failure mode

## False Reassurance Pattern

The system looks governed because there is evidence, documentation, and human
involvement. In practice, the real runtime remains weakly constrained.

## Minimal Assumptions

- the system performs or influences consequential runtime decisions
- governance claims are being made about that runtime
- effective preventive controls are absent or weak

## Where It Does Not Apply

This class is weaker when runtime policy bindings, preventive controls, and
effective intervention paths are explicit and challengeable.

## Typical Cases

- policy PDF with no execution binding
- evidence after action treated as governance
- human oversight as ceremony

## Mitigations

- bind policy to runtime execution
- separate preventive control from retrospective evidence
- test human oversight effectiveness rather than its nominal presence

## Residual Risk

Even strong runtime control cannot eliminate all failure. It can, however,
prevent governance from collapsing into theater.
