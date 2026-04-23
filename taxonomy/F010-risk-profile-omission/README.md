# F010 — Risk-Profile Omission

## Claim

A governance or safety framework can be structurally incomplete when it does
not produce a concrete, deployment-specific risk profile for the system it is
supposed to govern.

## Mechanism

The failure arises when:

- the framework stays at the level of principles or controls
- no deployment-specific risk articulation is required
- composition effects are not assessed
- advisory and execution systems are discussed with the same abstractions

## Observable Signature

- strong framework prose with weak system-specific risk articulation
- missing blast-radius or composition analysis
- abstract controls not mapped to deployed authority surfaces

## False Reassurance Pattern

The framework looks mature because it is detailed and structured. In practice,
decision-makers still do not know the concrete risk profile of the deployed
system.

## Minimal Assumptions

- a framework or governance method is being applied
- the governed system has meaningful deployment-specific risk variation
- the method does not require a concrete risk profile

## Where It Does Not Apply

This class is weaker when the framework requires a deployment-specific risk
profile and composition-aware blast-radius assessment.

## Typical Cases

- framework without risk profile
- governance methods that ignore composition and reversibility

## Mitigations

- require per-system risk profiles
- assess composition, consequence, reach, coupling, and reversibility
- trace framework claims to deployed properties

## Residual Risk

Risk profiles are still simplifications. The point is not perfect prediction,
but avoiding governance without deployment reality.
