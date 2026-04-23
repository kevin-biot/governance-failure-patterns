# Pattern — Data Governance Shape

## Purpose

Data governance becomes structurally real when governance metadata travels with
the governed object rather than living only in adjacent policy prose.

## Core moves

- require governance metadata on write or creation
- preserve that metadata across copy, move, replication, export, and deletion
- bind access decisions to policy, usage, consent, or purpose references
- fail deterministically when mandatory governance metadata is missing
- emit evidence for access, mutation, refusal, and transfer actions

## What this prevents

- data governance that disappears during movement
- residency or retention claims that are not attached to the data surface
- silent metadata stripping in portability paths
- weaker forms of `AP015` Framework Without Risk Profile

## Minimal artefacts

- jurisdiction or residency field
- retention or expiry field
- integrity field
- policy or usage reference
- evidence pointer or equivalent audit hook

## Working question

If this data object moves across systems or providers, what governance fields
move with it and what breaks if they do not?

## Boundaries

This shape does not require one storage protocol. It requires that governance
survive storage and movement rather than vanish at the API boundary.
