# Pattern — Sovereignty Requires Verifier-Friendly Evidence

## Purpose

This pattern responds to a common weakness in sovereignty language:

- sovereignty is asserted through branding, geography, or hosting posture
- but the claim is not exported in a form that a verifier can actually test

The design claim is:

**sovereignty becomes governance-grade only when it is joined to
verifier-friendly evidence.**

If the claim cannot be exported, replayed, and challenged, it is closer to
positioning than to governance.

## What this pattern requires

- explicit authority bindings for governed actions
- deterministic policy snapshots rather than mutable policy lore
- refusal semantics that are first-class and evidentiary
- evidence bundles that a third party can inspect without private tribal
  context
- claim discipline that distinguishes architecture intent from verified runtime
  posture

## What this prevents

- sovereignty by branding alone
- portability or auditability claims that cannot be independently checked
- premature legitimacy for specification-heavy frameworks
- weaker forms of `AP015` Framework Without Risk Profile
- weaker forms of `AP016` Governance Without Lifecycle Validation

## Minimal artefacts

- an evidence profile or export shape
- verifier responsibilities and expected checks
- refusal evidence for actions that fail authority or policy conditions
- versioned policy and authority snapshots
- a claim rule stating what may be said publicly before conformance authority is
  mature

## Working question

For any sovereignty or portability claim, ask:

> what exact evidence would an external verifier need to confirm or reject this
> claim?

If the answer is vague, the governance layer is not finished.

## Boundaries

Verifier-friendly evidence does not solve every sovereignty problem.

It does not decide:

- political legitimacy
- procurement strategy
- competitive positioning
- final legal interpretation

Its job is narrower and crucial:

> to stop sovereignty from collapsing into self-description
