# Governance Failure Patterns — Conformance Specification

*Machine-readable and procedure-shaped artefacts for testing governance
fragility, not only naming it.*

**Spec version:** 0.1
**Date:** 2026-04-23

---

## Why this directory exists

The repository already names:

- failure classes
- anti-patterns
- case studies

That is necessary but insufficient.

Deployers, auditors, policy teams, and researchers also need:

- a standard profile shape for recording exposure
- a way to encode governance shape, operating envelope, and risk profile
- named tests that can challenge anti-pattern claims
- a repeatable attestation format
- reusable report structures for findings and remediation

This directory is the first pass at that layer.

## Core idea

Anti-patterns should not remain prose labels. They should become challengeable
claims.

Each conformance test in this spec asks a bounded question:

- does the anti-pattern appear to be present?
- what evidence supports that judgment?
- what procedure could falsify or weaken the claim?
- what would count as passing, failing, or indeterminate?

## Contents

| File | Purpose | Status |
|---|---|---|
| `gf-profile.schema.json` | JSON Schema for a governance fragility profile | v0.1 |
| `anti-pattern-conformance-tests.md` | Named test procedures for current anti-patterns | v0.1 |
| `attestation-format.md` | Signed findings shape for a governance fragility attestation | v0.1 |
| `examples/` | Worked example profiles showing how the schema is intended to be used | v0.1 |

## Design principles

**Forms, not implementations.**
The spec describes what a governance-fragility assessment should look like. It
does not require a specific harness, vendor, or runtime.

**Evidence levels are explicit.**
Every strong claim should state whether it rests on:

- public source review
- architecture inspection
- replayable measurement
- perturbation testing
- private internal evidence

**Pass/fail is not always binary.**
Some governance tests will produce:

- `pass`
- `fail`
- `indeterminate`

Indeterminate is allowed when the evidence is weak, the artefacts are missing,
or the system was not instrumented well enough to answer honestly.

**Non-public research is usable but must be marked.**
Some tests may be informed by non-public research, but profiles and
attestations must mark that evidence level rather than laundering it into a
public-looking fact.

## How to use

### As a deployer or research team

1. Identify which anti-patterns are in scope.
2. Run the applicable tests in `anti-pattern-conformance-tests.md`.
3. Record findings in a profile shaped by `gf-profile.schema.json`.
4. Produce a written report using the templates under `../reports/templates/`.
5. Optionally sign the findings using `attestation-format.md`.

### As an auditor or reviewer

1. Retrieve the profile and supporting report.
2. Validate the profile against `gf-profile.schema.json`.
3. Re-run at least one test for each anti-pattern marked `present` or
   `demoted`.
4. Challenge the evidence level when the claim is stronger than the evidence.
5. Record any disagreements as findings against the profile.

## What this spec does not yet cover

- a reference harness for running tests automatically
- a full scoring model across multiple anti-patterns
- certification semantics or counter-signature workflow
- revocation or expiry registry for attestations
- sector-specific overlays for domains like health, finance, or public policy

Those can come later. v0.1 is about making the repository operational.
