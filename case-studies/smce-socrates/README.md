# Case Study — SMCE/SOCRATES

## Why This Case Exists

This case is a bounded example of how a serious formal policy tool can still be
fragile at the normative and monitoring layers.

It is also a useful first case because it contains all three elements that this
repository cares about:

- a real and non-trivial formal method
- an institutional ambition to support consequential policymaking
- a newer AI-assisted extension that appears to widen reach faster than it
  widens governance assurance

This makes the case analytically richer than a simple "bad dashboard" example.

## Relevant Classes

- `F001` Formal Transparency Without Foundational Adequacy
- `F002` Absorbed Drift and Baseline Laundering
- `F003` Entrained Consensus Mistaken for Validation
- `F004` Coupled Reasoning Collapse

## Public Source Pack

All public-source claims in this case were double-checked on 2026-04-23 against
official JRC / European Commission sources listed in
[../../evidence/notes/smce-socrates-source-pack.md](../../evidence/notes/smce-socrates-source-pack.md).

## Summary Judgment

SMCE/SOCRATES is a serious decision-analytic framework. The public JRC material
supports that narrow claim.

The same public material does **not** justify a stronger claim that the method
is an adequate foundation for policy legitimacy or that its newer AI-assisted
extensions remove the upstream fragility of framing, stakeholder selection,
time-horizon construction, or value encoding.

The most constructive reading is:

- the framework is stronger than ordinary dashboards
- the monitoring layer remains weaker than it looks
- the AI-assisted layer increases fragility at the framing surface
- a bounded tightening path is plausible

## What the Sources Say

### 1. The formal core is real

The official SOCRATES page says the tool implements the Social Multi-Criteria
Evaluation framework for ex-ante impact assessment, with three main components:

- multi-criteria analysis
- equity analysis
- sensitivity analysis

The same source states that the impact matrix can include quantitative and
qualitative measurements and that rankings are computed using the Kemeny
non-compensatory aggregation rule. It also states that the objective is **not**
to substitute policymakers but to improve understanding of assumptions,
uncertainty, robustness, and defensibility.

Source:

- Knowledge4Policy SOCRATES page, last updated 27 Feb 2026

### 2. The intergenerational-fairness extension is active and public-facing

The JRC intergenerational fairness page states that:

- a future `Intergenerational Fairness Monitoring Tool` is planned
- `Futures Balance` is an AI-assisted tool in prototyping phase
- the tool is grounded in SMCE and aimed at making long-term trade-offs and
  intergenerational impacts explicit

The associated policy brief states that:

- Futures Balance remains interoperable with SOCRATES rather than replacing it
- it is a prototype
- iterative reliability improvements are underway
- it supports problem framing, objective setting, criteria definition, and
  initial option development
- it is restricted to exploratory use and human-in-the-loop operation

Sources:

- JRC intergenerational fairness page
- Futures Balance policy brief

### 3. The monitoring/dashboard layer uses pooled relative positioning

The 2025 SIWB report states that the dashboard presents countries through
relative positions in a pooled reference distribution made from all Member
States and all years in the reference period. It also states that:

- missing values were imputed so each country has values for all indicators and
  all years
- the synthetic indices are defined as the median of percentile positions
- the dashboard uses a five-colour scheme for communication

The same report notes that the dashboard is intended as a central monitoring
tool for sustainable and inclusive wellbeing.

Source:

- SIWB dashboard report (JRC140456, 2025)

## What This Repository Infers

The following are analytic inferences from the source pack, not verbatim JRC
claims.

### Inference A — The method is better than ordinary dashboards but weaker than its policy role

Because SOCRATES has an explicit mathematical structure, handles heterogeneous
inputs, separates social-actor evaluation from technical evidence, and performs
sensitivity analysis, it is stronger than many institutional scoreboards.

But because the most important normative decisions still occur before the model
is populated, the method is too weak to carry legitimacy on its own.

This is the classic `F001` pattern.

### Inference B — The monitoring layer is vulnerable to absorbed drift

A pooled percentile dashboard is good at showing relative standing. It is not
the same thing as structural drift diagnosis.

If the reference frame moves with the system, or if imputation smooths
discontinuities, then long-horizon deterioration can be normalized by the
monitoring surface itself.

This is the `F002` pattern.

### Inference C — The AI-assisted extension shifts fragility upstream

The Futures Balance brief explicitly places AI assistance into:

- problem framing
- objective setting
- criteria definition
- option development

Those are exactly the most normatively consequential parts of the process.

Even with human-in-the-loop safeguards, that creates a new risk surface:
apparent coherence in the framing layer can be mistaken for validity.

This is where `F003` and `F004` become relevant.

### Inference D — Consensus can become less trustworthy as the process becomes more polished

Once a policy team shares:

- the same source pack
- the same institutional language
- the same AI-assisted drafting environment
- the same candidate option set

internal agreement can reflect entrainment rather than independent validation.

The more polished the process becomes, the more easily it can hide narrowing at
the framing layer.

This is not proven by the SOCRATES sources alone. It is an analogy supported by
the separate coupled-collapse literature and should be treated as such.

## Class Mapping

### `F001` Formal Transparency Without Foundational Adequacy

Why it fits:

- the formal core is explicit
- upstream framing, admissibility, and value choices remain under-governed
- the overall process can therefore look more justified than it really is

### `F002` Absorbed Drift and Baseline Laundering

Why it fits:

- the SIWB dashboard uses pooled relative positions across countries and years
- missing values are imputed for balanced indices
- synthetic indices compress many indicators into percentile-based summaries

These are exactly the conditions under which slow structural deterioration can
become harder to see.

### `F003` Entrained Consensus Mistaken for Validation

Why it may fit:

- AI-assisted framing is introduced into problem construction
- the process remains institutionally shared and iterative
- consensus inside that coupled environment may not be independent validation

This is a plausible risk class, not a source-proven fact about current JRC
practice.

### `F004` Coupled Reasoning Collapse

Why it may fit:

- if iterative AI-assisted framing becomes part of the policy workflow
- and if later outputs depend recursively on earlier AI-generated framings
- and if there is no strong external error signal

then small framing perturbations could produce abrupt recommendation shifts
rather than graceful change.

Again, this is an analogy, not a direct empirical claim about current JRC
operations.

## Bounded Tightening Path

The purpose of this repository is not only to identify fragility but also to
point at repair.

For this case, the tightening path has two layers.

### 1. Normative tightening

Add an upper governance layer:

- normative charter
- stakeholder admissibility register
- omission register
- time-horizon covenant
- counter-frame record
- decision provenance record

This addresses the `F001` problem directly.

### 2. Analytic tightening

Replace dashboard-only monitoring with a stronger state-detection layer.

A PSH-style substrate would help by adding:

- baseline-relative and externally anchored state estimates
- explicit drift-rate measures
- prediction horizon
- coherence / coupling integrity
- detection of weak pre-threshold deterioration

Selective predator-prey-style overlays could further help in domains where
interaction regimes matter more than static scores.

See:

- [../agent-chains/README.md](../agent-chains/README.md) for the coupled-collapse lineage
- [../../patterns/README.md](../../patterns/README.md) for mitigation pattern placeholders

## Boundaries

This case study does **not** claim:

- that SMCE/SOCRATES is pseudo-science
- that JRC currently uses AI for autonomous policymaking
- that every dashboard or composite index is invalid
- that all policy tools need a predator-prey overlay

It claims something narrower:

> a serious formal policy tool can still be too weak to carry legitimacy, too
> relative to diagnose absorbed drift, and newly fragile when AI is inserted
> into the framing layer faster than governance assurance is expanded

## Editorial Constraint

This case should remain class-first. It is not an anti-JRC dossier.
