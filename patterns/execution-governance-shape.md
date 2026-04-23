# Pattern — Execution Governance Shape

## Purpose

Execution is not neutral. The runtime form of a workload and the gate that
admits it are governance surfaces.

## Core moves

- require a declared execution envelope or runtime profile
- validate that declaration through an admission gate
- bind stronger isolation or attestation requirements to named policy triggers
- declare critical execution dependencies explicitly
- fail closed when the required policy or authority context is unavailable

## What this prevents

- runtime posture chosen implicitly by convenience
- stronger isolation becoming optional under pressure
- hidden dependency paths undermining the claimed control model
- weaker forms of `AP016` Governance Without Lifecycle Validation

## Minimal artefacts

- execution envelope declaration
- admission decision record
- policy trigger for stronger isolation when applicable
- dependency declaration
- attestation or integrity evidence where relevant

## Working question

What runtime form was approved, why was it approved, and what policy would have
refused a weaker form?

## Boundaries

This shape does not prescribe containers, VMs, or TEEs. It says the selected
runtime posture should be governed explicitly, not inherited accidentally.
