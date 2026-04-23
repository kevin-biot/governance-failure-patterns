# Governance Failure Patterns and Blast Radius Framework

## Purpose

This note explains how `governance-failure-patterns` relates to the sibling
repository `blast-radius-framework`.

They are adjacent, but they are not substitutes for one another.

## Short version

- **Blast Radius Framework (BRF)** classifies the operational blast surface of a
  deployed agentic system.
- **Governance Failure Patterns (GFP)** names the recurring governance weakness
  patterns that often explain why systems are weakly controlled, misleadingly
  governed, or difficult to audit.

The cleanest summary is:

> BRF rates deployed-system blast properties. GFP diagnoses governance weakness
> patterns and proposes tightening paths.

## Different unit of analysis

### BRF

BRF's primary unit is the deployed system.

It asks questions such as:

- how much authority does this system have?
- how far can it reach?
- how tightly is it coupled?
- how reversible are its actions?
- what is the consequence class?
- how observable is it?

It then turns those answers into:

- a BR class
- invariant conformance claims
- attested evidence

### GFP

GFP's primary unit is the governance weakness.

It asks questions such as:

- what recurring failure class is visible?
- what anti-pattern is instantiating it?
- what evidence supports that interpretation?
- what constructive pattern would tighten it?

It then turns those answers into:

- a failure interpretation
- anti-pattern linkage
- conformance questions
- mitigation patterns

## How they mesh

The repositories fit together in a practical sequence:

1. **Classify with BRF**
   Determine the deployed system's operational blast surface.

2. **Diagnose with GFP**
   Explain the governance weakness patterns that may underlie failed invariants,
   weak evidence, or unstable composition.

3. **Tighten with GFP constructive patterns**
   Use governance patterns and reference governance shapes to design
   remediation.

4. **Re-assess with BRF**
   Re-rate the system after architectural or governance changes.

## Where the overlap is useful

There are natural bridges between the two repos.

### BRF invariant failure -> GFP anti-pattern diagnosis

If a BRF invariant fails, GFP often helps explain why.

Examples:

- weak evidence binding or weak audit posture -> `F007`, `AP008`,
  `evidence governance shape`
- high coupling and unstable peer interaction -> `F003`, `F004`, `AP006`,
  `bounded AI role`
- stale validation or runtime drift -> `F009`, `AP014`,
  `governance lifecycle validation`

### BRF profile -> GFP remediation layer

A BR profile can say:

- what the blast surface is
- what evidence supports the rating

GFP can then add:

- what governance failure pattern is visible
- which anti-pattern is likely in play
- what design tightening path is appropriate

## Non-equivalence

The relationship should stay explicit:

- GFP is not a subset of BRF
- BRF is not merely one application of GFP
- a system can have a BR profile without a detailed governance-failure
  diagnosis
- a governance failure class can exist without being translated into a BR score

## Suggested wording

The safest summary for public readers is:

> Blast Radius Framework is the companion rating layer for deployed systems.
> Governance Failure Patterns is the companion diagnosis layer for governance
> weakness.

## Why keep both public

Keeping both repositories public makes the stack clearer:

- BRF answers the rating and attestation question
- GFP answers the governance diagnosis and mitigation question

Together they give a stronger public grammar for:

- what a system is operationally capable of damaging
- why its governance may still be weaker than it appears
