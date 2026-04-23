# Anti-Pattern Conformance Tests

*Named challenge procedures for the current governance anti-pattern catalogue.*

**Version:** 0.1
**Date:** 2026-04-23

---

## Purpose

This document gives each anti-pattern one or more stable challenge procedures.

Each test has:

- **Test ID**
- **What it verifies**
- **Procedure**
- **Pass criterion**
- **Evidence mode**

The goal is not fake precision. The goal is repeatable scrutiny.

## How to read results

- `pass` means the anti-pattern was challenged and the system resisted on that
  dimension
- `fail` means the anti-pattern is evidenced on that dimension
- `indeterminate` means the artefacts or instrumentation were not sufficient to
  answer honestly

---

## AP001 — Dashboard Legitimacy Laundering

### AP001-T1 — Normative artefact presence

**Verifies:** whether the dashboard is governed by explicit upstream normative
artefacts rather than functioning as de facto justification.

**Procedure:**
1. Request the normative charter, stakeholder register, and omission register.
2. Check whether those artefacts pre-date the dashboard deployment or scoring
   cycle.
3. Compare the dashboard outputs with those artefacts for consistency.

**Pass criterion:** all three artefacts exist, are versioned, and were not
authored only after the dashboard was already in operational use.

**Evidence mode:** documentary review.

### AP001-T2 — Composite-first presentation check

**Verifies:** whether summary scores are presented before their framing limits.

**Procedure:**
1. Review the dashboard's opening page, executive deck, or public-facing entry
   point.
2. Record whether composite scores or color bands appear before framing,
   omission, and weighting notes.

**Pass criterion:** framing limits and omissions are visible at or before the
first summary score surface.

**Evidence mode:** interface and document inspection.

---

## AP002 — Pooled Baseline Drift Masking

### AP002-T1 — Frozen-baseline replay

**Verifies:** whether deterioration disappears when the reference frame moves
with the system.

**Procedure:**
1. Select a historical period with enough observations to compare.
2. Recompute the monitoring output using:
   - the deployed moving or pooled baseline
   - a frozen external baseline
3. Compare directional conclusions.

**Pass criterion:** materially important deterioration is not erased by the
moving baseline.

**Evidence mode:** replay test.

### AP002-T2 — Absolute vs relative view parity

**Verifies:** whether the system keeps absolute trend views separate from
relative rank views.

**Procedure:**
1. Inspect the reporting outputs.
2. Check whether absolute trend lines are available beside percentile or rank
   views.
3. Check whether important decisions rely only on relative position.

**Pass criterion:** absolute and relative views are both present and neither is
silently substituted for the other.

**Evidence mode:** document and interface inspection.

---

## AP003 — AI Consensus as Validation

### AP003-T1 — Independence challenge

**Verifies:** whether apparent agreement rests on genuinely independent
evidence paths.

**Procedure:**
1. Identify the models, prompt families, source packs, and synthesis loops used
   by each participant or agent.
2. Record how much of that substrate is shared.
3. Check whether the system treats convergence as stronger than its actual
   independence warrants.

**Pass criterion:** agreement is not represented as independent validation when
the evidence path is substantially shared.

**Evidence mode:** architecture and process inspection.

### AP003-T2 — Counter-frame requirement

**Verifies:** whether the process forces a rival framing before treating
convergence as robust.

**Procedure:**
1. Inspect the assessment or policy workflow.
2. Determine whether at least one counter-frame, counter-pack, or rival
   synthesis pass is mandatory.

**Pass criterion:** a counter-frame is required for consequential decisions.

**Evidence mode:** process review.

---

## AP004 — Constitution After the Model

### AP004-T1 — Chronology test

**Verifies:** whether normative governance artefacts were written before the
analytic model became operational.

**Procedure:**
1. Retrieve timestamps or version history for:
   - the model or framework deployment
   - the normative charter
   - stakeholder admissibility and omission artefacts
2. Compare ordering.

**Pass criterion:** the constitutional artefacts pre-date operational scoring
or ranking.

**Evidence mode:** document and version-history review.

### AP004-T2 — Model-authored constitution check

**Verifies:** whether governance language merely ratifies an existing tool.

**Procedure:**
1. Compare constitutional language with the model's existing indicator set,
   weight structure, or category logic.
2. Check whether governance documentation explains why the frame was chosen, or
   only restates the frame already embedded in the tool.

**Pass criterion:** the constitutional layer governs the tool rather than
post-rationalizing it.

**Evidence mode:** documentary and structural comparison.

---

## AP005 — Markov Without Transition-Drift Detection

### AP005-T1 — Transition-drift instrumentation check

**Verifies:** whether the system explicitly monitors transition drift rather
than only emitting state probabilities.

**Procedure:**
1. Inspect the state-model monitoring design.
2. Check for:
   - transition-matrix drift checks
   - residual drift tracking
   - changepoint or regime-break diagnostics

**Pass criterion:** at least one explicit transition-drift diagnostic is in
routine use.

**Evidence mode:** architecture and measurement inspection.

### AP005-T2 — Horizon divergence test

**Verifies:** whether one-step fit hides long-horizon degradation.

**Procedure:**
1. Evaluate short-horizon predictive performance.
2. Evaluate longer-horizon performance or stability.
3. Compare whether the model remains apparently healthy only at short horizon.

**Pass criterion:** no material divergence exists between short-horizon fit and
the system's longer-horizon behavior without a surfaced warning.

**Evidence mode:** replay or validation test.

---

## AP006 — Natural-Language Peer Coupling

### AP006-T1 — Consequential peer-edge mapping

**Verifies:** whether consequential peer-to-peer handoffs are free-form natural
language by default.

**Procedure:**
1. Map the system's peer edges.
2. Identify which edges carry control-relevant content.
3. Classify each edge as:
   - typed or schema-bounded
   - mixed
   - free-form natural language

**Pass criterion:** consequential peer edges are not predominantly free-form
natural language.

**Evidence mode:** architecture inspection.

### AP006-T2 — Coupling under perturbation

**Verifies:** whether agreement and coupling intensify under perturbation while
remaining weakly grounded.

**Procedure:**
1. Run a bounded perturbation, fork, or replay challenge.
2. Observe overlap, repetition, or convergence behavior across peers.
3. Compare the coupling signal with external grounding or truth conditions.

**Pass criterion:** perturbation does not create synchronized convergence or
collapse without external correction.

**Evidence mode:** perturbation test.

### AP006-T3 — Probe dissociation check

**Verifies:** whether internal probes remain green while behavioral quality
degrades.

**Procedure:**
1. Compare internal monitoring or probe success with substantive task quality
   during a challenge run.
2. Record whether probe health and actual behavior diverge.

**Pass criterion:** monitoring and substantive quality remain aligned closely
enough that internal probes are not falsely reassuring.

**Evidence mode:** perturbation or replay test.

---

## Open question

v0.1 gives each current anti-pattern at least two challenge paths where
possible. A later version should add:

- sector overlays
- stronger quantitative thresholds
- cross-anti-pattern bundle tests
- example profiles showing real pass/fail results
