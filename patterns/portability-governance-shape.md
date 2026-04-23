# Pattern — Portability Governance Shape

## Purpose

Governance is incomplete if it only works in steady state inside one provider
or one deployment.

Portability is a governance surface because authority, policy, evidence, and
constraints must survive migration and exit.

## Core moves

- export workloads, data, policy snapshots, and evidence together where needed
- validate governance posture before governed execution resumes on the target
- preserve governance metadata across export and import
- declare non-substitutable dependencies explicitly
- support rollback or refusal when validation fails

## What this prevents

- portability that moves compute but drops governance semantics
- migration claims without enforceable target-state validation
- exit plans that lose evidence or policy history
- weaker forms of `AP015` Framework Without Risk Profile

## Minimal artefacts

- migration or export bundle
- policy and authority snapshot portability
- validation-before-resume rule
- dependency manifest
- rollback or refusal path with evidence

## Working question

If this system moves, what guarantees that its governance posture moves with
it?

## Boundaries

This shape does not promise universal portability. It requires that portability
limits be declared and that unsupported moves fail visibly rather than pretend
to preserve governance.
