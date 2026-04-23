# Example Crosswalk — Accountability Displacement Interpretation

## Source stub

- Source system: AI Incident Database
- Record type: illustrative agentic commerce or delegated automation case
- Public signal: technical traceability exists, but responsible-principal
  accountability remains weak or unclear

## Observed outcome

The public incident record suggests a consequential automated action where the
system can identify the technical actor or credential path more easily than it
can identify the accountable principal behind the action.

## Governance interpretation

The likely governance weakness is not lack of traceability in the narrow
technical sense.

It is:

- accountability displaced into the credential or agent layer
- insufficient clarity about scope, revocation, or dispute-grade evidence
- trust language stronger than explicit risk framing

## Candidate failure classes

- `F008` Accountability Displacement
- `F010` Risk-Profile Omission

## Candidate anti-patterns

- `AP017` Agent Keys as Legal Personhood
- `AP015` Framework Without Risk Profile

## Candidate constructive patterns

- `delegated agent identity`
- `interface governance shape`
- `normative charter`

## Candidate mitigations

- bind technical identity explicitly to a responsible principal
- make delegation scope, expiry, and revocation first-class
- require dispute-grade evidence that reaches beyond the agent credential

## Confidence

`medium`

The accountability interpretation is plausible from public material, but the
incident record may not expose the full contractual or identity architecture.
