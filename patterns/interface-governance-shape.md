# Pattern — Interface Governance Shape

## Purpose

Interfaces are governance surfaces when they carry authority, delegated scope,
refusal semantics, and evidence hooks rather than bare invocation alone.

## Core moves

- expose delegated scope explicitly for consequential calls
- make refusal and error semantics governance-aware, not merely transport-level
- preserve evidence pointers or audit references in consequential outcomes
- separate portable resource shape from provider-private convenience behavior
- make unsupported actions fail visibly rather than degrade silently

## What this prevents

- API surfaces that hide delegated authority assumptions
- refusal treated as an implementation detail rather than a governance event
- provider-specific behavior masquerading as portable governance
- weaker forms of `AP010` Capability Discovery as Attack Surface

## Minimal artefacts

- delegated scope or authority reference
- refusal/error model
- evidence hook or pointer
- portable resource contract
- versioning and compatibility rule

## Working question

Does this interface merely expose functionality, or does it expose the
governance conditions under which that functionality may be used?

## Boundaries

Not every API needs the same depth of governance semantics. The point is that
consequential interfaces should not hide them completely.
