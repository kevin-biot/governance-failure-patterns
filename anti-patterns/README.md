# Anti-Patterns

This directory names deployer-visible bad habits, architectural moves, and
workflow choices that inflate governance fragility by design.

If `taxonomy/` contains the deeper failure classes, `anti-patterns/` is the
practical front-end:

- what people ship
- what institutions praise as progress
- what silently amplifies the underlying failure classes

## Relationship to the Sibling Blast-Radius Work

This surface is intentionally inspired by the structure of the sibling
`blast-radius-framework` anti-pattern catalogue, but it is **not** a copy.

The blast-radius catalogue is oriented toward:

- operational blast radius
- agentic system risk
- architectural and evidence-chain escalation

This repository's anti-pattern surface is oriented toward:

- policy tooling
- governance fragility
- legitimacy laundering
- monitoring weakness
- AI-assisted framing failure

The shared idea is useful:

- name the anti-pattern
- state the mechanism
- state the visible damage
- state the remediation path

## Current Seed Anti-Patterns

- `AP001` Dashboard Legitimacy Laundering
- `AP002` Pooled Baseline Drift Masking
- `AP003` AI Consensus as Validation
- `AP004` Constitution After the Model

## How to Read an Entry

Each entry should contain:

- name
- mechanism
- failure-class linkage
- visible signature
- false reassurance pattern
- demotion path

Use [../templates/anti-pattern-template.md](../templates/anti-pattern-template.md)
for new entries.
