# Pattern — Policy as Runtime

## Purpose

This pattern answers a recurring governance failure:

> the institution has a policy, but the runtime system is not actually governed
> by it

The design claim is simple:

**policy only counts as governance when it binds the runtime behavior of the
system.**

## Core moves

- version policy as an explicit epoch rather than a floating document
- bind decisions or executions to the policy epoch in force
- make consequential policy claims challengeable through runtime tests
- distinguish narrative guidance from executable constraint

## What this prevents

- `AP007` Policy PDF, Runtime Nothing
- weaker forms of `AP004` Constitution After the Model
- informal policy drift through prompts, overrides, and habits

## Minimal artefacts

- policy snapshot or epoch identifier
- explicit control-point map showing where policy is enforced
- runtime decision record or execution record bound to the active policy
- challenge tests for critical policy claims

## Boundaries

Policy as runtime does not mean every value judgment is machine-enforced.
Normative choices still need human governance. The point is narrower: where the
institution claims a rule constrains execution, that claim should survive
runtime challenge.
