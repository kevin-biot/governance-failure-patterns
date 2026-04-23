# Contributing

Thanks for improving the repository.

This project is not a general opinion archive. It is a bounded, public-interest
taxonomy and conformance method for governance failure patterns.

## Contribution priorities

The most useful contributions are:

- new failure classes with clear boundaries
- anti-patterns tied to challengeable tests
- case studies with explicit source/inference separation
- spec improvements that make claims more falsifiable
- corrections that tighten language, evidence quality, or public readability

## What to avoid

Please do not submit:

- vendor takedowns framed as taxonomy entries
- unbounded claims about entire sectors or institutions
- private or proprietary implementation detail that is not already public
- case studies that cannot distinguish observation from inference
- mitigation-free critique

## Required standards

Every substantive contribution should be:

- class-first, not enemy-first
- bounded, not totalizing
- evidence-aware, not rhetorical
- repair-oriented, not merely oppositional

See:

- [editorial-policy.md](./editorial-policy.md)
- [PUBLICATION-STANDARD.md](./PUBLICATION-STANDARD.md)

## Claim classes

When adding or revising content, be explicit about the claim type:

- `source-backed`
  Grounded directly in cited public material.
- `analytic inference`
  A bounded interpretation drawn from source-backed material.
- `private-internal provisional`
  Informed by private research not yet publicly reproducible.

Do not blur these classes together.

## Where to put things

- `taxonomy/`
  Deeper recurrent failure classes.
- `anti-patterns/`
  Deployer-visible bad habits or architectural moves.
- `case-studies/`
  Bounded analyses of public or generalized examples.
- `patterns/`
  Repair notes and constructive mitigation shapes.
- `evidence/notes/`
  Source packs, provenance notes, and evidence-boundary records.
- `spec/`
  Schema, tests, attestation shapes, and examples.

## Minimal bar for a new entry

### New failure class

- mechanism is stated
- signatures are visible
- false reassurance pattern is named
- boundaries or non-applicability are stated
- at least one mitigation path exists

### New anti-pattern

- linked to one or more failure classes
- has at least one challengeable test
- does not overclaim beyond the available evidence

### New case study

- sources are cited
- inference is separated from source-backed claims
- unknowns are kept explicit
- the case is reusable beyond one vendor whenever possible

## Versioning and change control

This repository uses lightweight semantic versioning for public releases:

- `MAJOR`
  Structural reset, incompatible reorganization, or framework-level change.
- `MINOR`
  New taxonomy families, anti-pattern families, spec fields, or reporting
  surfaces.
- `PATCH`
  Clarifications, wording repairs, template cleanup, and non-structural fixes.

Public-facing changes should be logged in [CHANGELOG.md](./CHANGELOG.md).

## Proposed workflow

1. Open or use an issue.
2. State the problem in class language, not personality language.
3. Add or revise the relevant document.
4. Update templates or spec if the contribution changes authoring shape.
5. Update `CHANGELOG.md` for structural changes.
6. Re-read for evidence boundaries and public readability.

## Before a contribution is considered ready

Check that:

- private material has been removed or generalized
- the document is falsifiable enough to be challenged
- the mitigation path is not empty
- the language would be acceptable in a public-interest repository

If in doubt, tighten the claim rather than broadening it.
