# Governance Failure Patterns

Private incubation repository for a public-service taxonomy of governance
failure classes in AI-assisted decision systems, policy analytics, and related
public-interest tooling.

This repository starts private on purpose. The goal is to refine the taxonomy,
remove private or proprietary material, and generalize the patterns before
opening it publicly.

## Purpose

This repository exists to make governance failures legible as named, reusable
classes rather than isolated complaints.

The working thesis is simple:

- fragile governance patterns repeat across institutions and toolchains
- they are easier to debate once they are named and bounded
- public critique is stronger when paired with remediation patterns

This repository therefore aims to publish:

- failure classes
- anti-patterns
- case studies
- remediation patterns
- conformance methods
- templates for structured analysis

## Scope

The repository focuses on failure classes such as:

- formal transparency without foundational adequacy
- absorbed drift and baseline laundering
- entrained consensus mistaken for validation
- coupled reasoning collapse in AI-assisted framing
- stationarity fiction in state models
- omission invisibility
- missing-stakeholder laundering
- dashboard false reassurance
- static scoring that hides interaction regimes

## Working Rules

- No private DOP implementation detail should be copied in raw form.
- No private client or patient information should appear here.
- When a private insight is useful, it must be generalized into a class,
  mechanism, or abstracted case pattern.
- Each critique should aim to include a mitigation or tightening pattern.
- Every failure class should state where it does not apply.

See [editorial-policy.md](./editorial-policy.md).

## Repository Shape

- [framework.md](./framework.md) — what a governance failure class is and how
  the taxonomy works
- [taxonomy/](./taxonomy/) — named failure classes
- [anti-patterns/](./anti-patterns/) — named deployer-visible bad habits and
  architectural/process anti-patterns that instantiate or amplify the failure
  classes
- [case-studies/](./case-studies/) — bounded example analyses
  including `smce-socrates`, `agent-chains`, topology-focused coupling cases,
  runtime-governance cases, and generalized agent-accountability cases
- [patterns/](./patterns/) — remediation and tightening patterns
  including `policy as runtime`, `runtime evidence`, and `doctrine as coupling layer`
- [templates/](./templates/) — reusable authoring templates
- [spec/](./spec/) — profile shape, conformance tests, and attestation format
- [reports/templates/](./reports/templates/) — reusable findings and remediation
  report templates
- [evidence/](./evidence/) — notes, source references, and supporting material

## Initial Seed Set

- `F001` Formal Transparency Without Foundational Adequacy
- `F002` Absorbed Drift and Baseline Laundering
- `F003` Entrained Consensus Mistaken for Validation
- `F004` Coupled Reasoning Collapse
- `F005` Stationarity Fiction in State Models

## Status

Private incubation.

The immediate job is not scale. It is quality:

- sharpen the taxonomy
- remove private IP
- generalize the examples
- make the language fit for public dialogue
- make the anti-patterns testable
