# Pattern — Evidence Governance Shape

## Purpose

Evidence becomes governance-grade when it records the decision context, not
just the fact that something happened.

## Core moves

- record authority and policy snapshots in force at the time of action
- record refusal as a first-class outcome
- preserve ordering and integrity where governance claims depend on them
- export evidence in a form that a third party can inspect
- support replay, challenge, and verifier use rather than only internal search

## What this prevents

- descriptive logs mistaken for governance evidence
- policy-free audit trails
- post-hoc narratives that cannot be checked independently
- weaker forms of `AP008` Evidence After Action

## Minimal artefacts

- event or decision record
- authority snapshot id
- policy snapshot id
- refusal class or reason when applicable
- export path and integrity expectations

## Working question

If an external reviewer asks why this action was allowed or refused, what exact
artefact answers that question?

## Boundaries

Evidence does not replace control. It makes control and refusal challengeable
after the fact.
