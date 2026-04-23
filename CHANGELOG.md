# Changelog

All notable changes to this repository should be recorded here.

This changelog is intentionally structural rather than exhaustive. It tracks:

- new taxonomy classes
- new anti-patterns
- new case-study families
- spec and schema changes
- publication-standard changes

It does not need to list every wording tweak.

The format is inspired by Keep a Changelog, but adapted for a research and
governance-method repository.

## [Unreleased]

## [0.1.0] - 2026-04-23

### Added

- Root repository framing, editorial policy, and external-facing README.
- Release-discipline layer:
  - `CHANGELOG.md`
  - `CONTRIBUTING.md`
  - `PUBLICATION-STANDARD.md`
  - issue templates under `.github/ISSUE_TEMPLATE/`
- Seed taxonomy:
  - `F001` Formal Transparency Without Foundational Adequacy
  - `F002` Absorbed Drift and Baseline Laundering
  - `F003` Entrained Consensus Mistaken for Validation
  - `F004` Coupled Reasoning Collapse
  - `F005` Stationarity Fiction in State Models
  - `F006` Rulebook Without Doctrine
  - `F007` Runtime Governance Substitution
  - `F008` Accountability Displacement
  - `F009` Validation-Lifecycle Break
  - `F010` Risk-Profile Omission
- Anti-pattern catalogue through `AP017`.
- Spec layer:
  - `gf-profile.schema.json`
  - anti-pattern conformance tests
  - attestation format
  - worked examples
- Authoring templates and report templates.
- Initial case studies and provenance notes for:
  - SMCE/SOCRATES
  - agent chains / Sentinel-style coupling
  - topology as coupling surface
  - runtime governance
  - registered agent without delegated accountability
- Generalized sovereignty-governance extraction:
  - case study on specification-rich sovereignty frameworks
  - pattern note on verifier-friendly evidence for sovereignty claims
  - provenance note recording the public-source basis and claim posture
- Constructive governance-shape layer:
  - reference governance shapes overview
  - creation, data, execution, interface, evidence, and portability shape notes

### Notes

- `0.1.0` is the first structured release baseline for public visibility.
- The repository remains conservative about evidence boundaries:
  public source-backed claims, analytic inference, and private internal
  incubation should remain explicitly separated.
