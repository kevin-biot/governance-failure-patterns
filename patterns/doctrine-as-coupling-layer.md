# Pattern — Doctrine as Coupling Layer

## Purpose

This pattern addresses a macro-level governance failure:

> institutions can have many policies without having a coherent doctrine that
> keeps those policies aligned over time

The design claim is:

**doctrine is the coupling layer above the rulebook.**

It is what makes multiple instruments cohere rather than drift into a stack of
local optimizations and later repairs.

## What doctrine must do

A usable doctrine should make at least four things explicit:

- the enduring objective
- the principal contradiction, threat, or strategic tension
- the ranking of trade-offs when objectives collide
- the reason separate instruments belong to one operating logic

## What this prevents

- `AP011` Rulebook Without Doctrine
- weaker forms of policy-stack drift hidden by later simplification packages
- implementation guidance becoming de facto strategy by default

## Minimal artefacts

- a short doctrine statement that survives beyond one instrument
- an explicit trade-off hierarchy
- a cross-instrument mapping showing how each major policy fits the doctrine
- a review rule requiring new measures to justify doctrinal fit

## Boundaries

Doctrine is not a substitute for detailed policy or for democratic contest.
Its job is narrower: to keep a growing rule stack strategically coupled so that
later coherence does not depend on ad hoc repair alone.
