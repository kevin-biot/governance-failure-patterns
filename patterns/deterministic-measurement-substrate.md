# Pattern — Deterministic Measurement Substrate

## Purpose

Critical measurement and control claims should rest on a layer that can be
replayed and challenged independently of narrative or stochastic reasoning.

## Core moves

- keep consequential measurement logic deterministic where possible
- separate explanation layers from measurement layers
- version inputs, transforms, and outputs explicitly
- allow independent replay of key governance-relevant results

## What this prevents

- stochastic interpretation becoming hidden measurement authority
- narrative coherence being mistaken for measurement validity
- weaker forms of `F003` Entrained Consensus Mistaken for Validation

## Minimal artefacts

- declared inputs
- deterministic transform or rule set
- output record
- replay path

## Working question

What part of this governance claim can be recomputed independently?

## Boundaries

Not every part of a system must be deterministic. The point is that the core
measurement substrate for consequential claims should not be purely interpretive.
