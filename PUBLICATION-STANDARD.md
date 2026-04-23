# Publication Standard

This document defines the minimum bar for content that is ready to survive
public scrutiny.

It is stricter than a drafting note and lighter than formal peer review.

## Purpose

The repository is intended to become public-facing. That means each published
document should be able to withstand at least three kinds of challenge:

- factual challenge
- category challenge
- fairness challenge

The question is not only "is this interesting?" It is:

- is it bounded?
- is it supportable?
- is it fair?
- is it useful?

## Release gates

Before a document is treated as public-ready, it should pass all of these.

### Gate 1: Boundary hygiene

- private or proprietary implementation detail removed or generalized
- client, patient, or partner specificity removed unless already public
- no disguised leaks

### Gate 2: Claim discipline

- source-backed claims are cited
- analytic inference is clearly marked as inference
- private-internal provisional claims are labeled as such
- no rhetorical overreach beyond the evidence base

### Gate 3: Taxonomic usefulness

- the document names a reusable pattern or bounded case
- it is not merely a complaint about one organization
- the class or case is legible enough for others to challenge or reuse

### Gate 4: Repair path

- at least one mitigation, demotion, or tightening path is stated
- the note does not end at diagnosis alone

### Gate 5: Public readability

- language is intelligible to external readers
- internal shorthand is removed
- unnecessary private context is not required to understand the note

## Evidence classes

Every strong claim should be legible as one of:

- `source-backed`
- `analytic inference`
- `private-internal provisional`

If a note mixes them, the boundary must remain explicit.

## Change control

For public release discipline:

- structural changes should be logged in `CHANGELOG.md`
- releases should be tagged
- public versions should move under semantic versioning
- major claim changes should update the changelog even if the file path stays
  the same

## Versioning rule

Use lightweight semantic versioning:

- `MAJOR`
  Structural rewrite, taxonomy reset, or incompatible spec change.
- `MINOR`
  New classes, anti-pattern families, case-study families, or spec features.
- `PATCH`
  Clarifications, evidence-boundary cleanup, wording repairs, template fixes.

## Public release recommendation

The first public opening should be a tagged release, for example `v0.1.0`,
with:

- root README
- editorial policy
- contribution standard
- changelog
- publication standard
- seed taxonomy
- anti-pattern catalogue
- spec and examples

That gives external readers a stable reference point rather than a moving
private draft.
