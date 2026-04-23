# Pattern — Coherence Monitoring

## Purpose

Coherence monitoring watches for breakdown in relationships and structural fit,
not only threshold breaches in isolated metrics.

## Core moves

- monitor relationships between signals, not just individual values
- watch for pre-failure instability or thinning
- treat changed coupling structure as a governance-relevant event
- separate apparent surface stability from underlying structural drift

## What this prevents

- hidden deterioration masked by acceptable point metrics
- absorbed drift that only becomes visible after failure
- weaker forms of `F002` Absorbed Drift and Baseline Laundering

## Minimal artefacts

- relationship or coupling measure
- baseline coherence expectation
- drift or instability signal
- intervention rule when coherence breaks materially

## Working question

What relationships need to remain stable for this governance claim to stay
credible?

## Boundaries

Coherence is not the same as goodness. The point is to detect structural
breakdown earlier than isolated threshold alarms do.
