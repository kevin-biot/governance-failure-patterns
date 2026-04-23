# Governance Report Templates

*Three reusable report templates for applying the governance-failure method to
real systems and frameworks.*

**Template version:** 1.0
**For spec version:** 0.1

---

## The three tiers

| Template | Audience | Purpose |
|---|---|---|
| `executive-summary-template.md` | Executive, policy lead, procurement, board | Short explanation of what failed, why it matters, and what to do next |
| `technical-findings-template.md` | Architect, reviewer, auditor, researcher | Test-by-test findings and evidence shape |
| `remediation-backlog-template.md` | Delivery team, governance owner, architecture lead | Ordered demotion path for anti-patterns |

## How to use

1. Identify the in-scope anti-patterns.
2. Run the relevant tests from `../../spec/anti-pattern-conformance-tests.md`.
3. Record the findings in a machine-readable profile.
4. Populate the report templates from that profile.
5. If needed, issue a signed attestation.

## Design principle

These templates are intentionally parallel to the blast-radius report shape:

- one short executive surface
- one deeper technical surface
- one action-oriented remediation surface

The difference is that this repository is about governance fragility rather
than operational blast radius.
