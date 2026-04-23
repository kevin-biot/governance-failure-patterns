# Governance Fragility Attestation Format

*A minimal signed statement of what was tested, what was found, and how strong
the evidence is.*

**Version:** 0.1
**Date:** 2026-04-23

---

## Purpose

The repository needs a way to say:

- what system or framework was assessed
- which anti-patterns were tested
- what the results were
- what evidence level supports the claim
- what governance shape and operating envelope were assumed

without pretending to have a full certification regime.

This is that shape.

## Minimum attestation contents

An attestation should contain:

1. **Subject**
   - name
   - type
   - scope statement
   - version, if applicable

2. **Assessment metadata**
   - assessment date
   - assessor
   - method version
   - repository commit or report version

3. **Anti-pattern findings**
   - anti-pattern ID
   - status: `present`, `demoted`, `not_present`, or `indeterminate`
   - test IDs run
   - per-test results
   - summary finding

4. **Evidence declaration**
   - public
   - mixed
   - private internal
   - reproducible
   - attested

5. **Residual risk statement**
   - what remains unresolved even if the anti-pattern was partly demoted

6. **Lifecycle and validity**
   - governance shape assessed
   - operating envelope assumed
   - attestation expiry

## Suggested JSON envelope

```json
{
  "schema_version": "0.1",
  "attestation_type": "governance_fragility",
  "profile_ref": "gf-example-001",
  "subject": {
    "name": "Example Policy Tool",
    "type": "policy_tool",
    "version": "2026.04"
  },
  "assessment": {
    "date": "2026-04-23",
    "assessor": "Example Assessor",
    "method_version": "0.1"
  },
  "findings": [
    {
      "anti_pattern_id": "AP006",
      "status": "present",
      "evidence_level": "mixed",
      "tests": [
        { "test_id": "AP006-T1", "result": "fail" },
        { "test_id": "AP006-T2", "result": "indeterminate" }
      ],
      "summary": "Consequential peer edges are natural-language mediated."
    }
  ],
  "residual_risk": [
    "Monitoring remains weaker than the coupling surface requires."
  ]
}
```

## Signature guidance

v0.1 does not mandate a single signature stack.

It does require that any published attestation make the following explicit:

- who signed it
- which bytes were signed
- which verification method applies

Acceptable examples:

- a detached signature over the JSON document
- a signed Git tag naming the attested commit
- a DNS-, transparency-log-, or timestamp-anchored digest

## Honesty rule

An attestation must not imply stronger evidence than it has.

In particular:

- `public` means the claim can be grounded in public artefacts
- `mixed` means public and private evidence are both involved
- `private_internal` means the claim should not be treated as publicly
  established
- `reproducible` means another party could reasonably re-run the procedure
- `attested` means the finding has a stronger signed or independently checked
  form

## Expiry

Governance attestations should expire.

Suggested default:

- `180` days for static frameworks or published case studies
- `90` days for live systems or fast-moving agent architectures

If major architecture, model, or governance changes occur earlier, the
attestation should be considered stale immediately.
