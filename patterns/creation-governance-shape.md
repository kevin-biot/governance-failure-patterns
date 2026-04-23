# Pattern — Creation Governance Shape

## Purpose

Creation is a governance surface.

If a tenant, workspace, project, or similar governed object is created without
bound authority, scope, and baseline policy, later governance starts from an
already-weak foundation.

## Core moves

- require an authority binding at creation time
- attach a baseline policy or policy snapshot
- attach key scope fields such as jurisdiction, classification, or ceiling
- make refusal first-class when required fields are missing or invalid
- emit evidence for creation and refusal outcomes

## What this prevents

- governance retrofitted after object creation
- scope ambiguity at birth
- silent exception culture around bootstrap operations
- weaker forms of `AP004` Constitution After the Model

## Minimal artefacts

- authority reference or snapshot id
- baseline policy reference or snapshot id
- scope fields carried by the created object
- refusal reason when creation is blocked
- evidence of the creation decision

## Working question

When a governed object comes into existence, what exactly binds its authority,
scope, and baseline constraints from the first moment?

## Boundaries

Not every field must be enforced by the same system. The point is narrower:
creation should not be treated as a governance-free phase.
