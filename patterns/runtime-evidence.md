# Pattern — Runtime Evidence

## Purpose

This pattern distinguishes:

- evidence that something happened
- evidence that the system was governed while it was happening

The repository's stance is:

**runtime evidence should support accountability, but it should not be confused
with runtime control.**

## Core moves

- record the decision or execution state at the time of action
- preserve the binding between runtime evidence and the governing policy epoch
- separate preventive controls from retrospective logs
- make evidence useful for replay, challenge, and audit

## What this prevents

- `AP008` Evidence After Action
- weak forms of ceremonial governance built on logging alone

## Minimal artefacts

- runtime decision or execution record
- policy or rule binding at time of action
- evidence of whether a preventive control fired
- replayable artefacts where feasible

## Boundaries

Runtime evidence is necessary but not sufficient. A beautifully logged failure
is still a failure if the system had no realistic way to stop the action.
