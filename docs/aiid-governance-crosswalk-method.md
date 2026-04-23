# AI Incident Database to Governance Failure Patterns — Crosswalk Method

## Purpose

This note defines a bounded method for mapping public AI incident records into
the governance-failure-patterns taxonomy.

The point is not to overwrite incident taxonomies.

The point is to add a governance lens:

- incident taxonomies describe what happened
- this crosswalk suggests which governance failure classes or anti-patterns may
  help explain why the outcome was possible, weakly controlled, or hard to
  detect
- the pattern layer then suggests candidate mitigation shapes

## Source relationship

The [AI Incident Database](https://incidentdatabase.ai/) already applies public
taxonomies including:

- CSET AI Harm Taxonomy
- Goals, Methods, and Failures (GMF)
- MIT AI Risk Repository views such as domain, entity, timing, and intent

This method does not replace those structures.

It overlays them with:

- governance failure classes
- anti-patterns
- constructive patterns
- candidate mitigations

## Core rule

The crosswalk is interpretive and many-to-many.

It must not imply:

- that every incident has one definitive governance cause
- that the source incident database endorses the governance mapping
- that mitigation can be derived mechanically from the incident label alone

The crosswalk should instead state:

- likely governance interpretation
- confidence level
- ambiguity or missing information

## Recommended record shape

Each crosswalk record should include:

- `source_system`
- `source_record_id`
- `source_url`
- `source_taxonomies`
- `incident_summary`
- `observed_outcome`
- `candidate_failure_classes`
- `candidate_anti_patterns`
- `candidate_patterns`
- `candidate_mitigations`
- `mapping_confidence`
- `ambiguity_notes`

## Mapping steps

### 1. Start with the incident, not the theory

Read the incident summary and source taxonomy labels first.

Do not begin by hunting for a favorite anti-pattern.

### 2. Separate outcome from governance interpretation

Record:

- what happened
- what the source taxonomy says
- what governance interpretation is being inferred

These are not the same thing.

### 3. Map to failure classes before anti-patterns

Prefer:

- deeper failure class first
- visible anti-pattern second
- mitigation pattern third

This keeps the mapping principled rather than slogan-driven.

### 4. Keep mitigation bounded

Do not jump from an incident to a maximal redesign.

State candidate mitigation shapes that are plausibly responsive to the observed
governance weakness.

### 5. Add confidence explicitly

Confidence should reflect how much the public incident record actually supports
the governance inference.

## Confidence rubric

### High

Use `high` when:

- the incident text directly supports the governance interpretation
- the anti-pattern is visible in the public record
- little interpretive stretching is required

### Medium

Use `medium` when:

- the governance interpretation is plausible and well-motivated
- but the public incident does not fully expose the internal control surface

### Low

Use `low` when:

- the outcome is public
- but the governance interpretation depends heavily on missing internal detail

## Example mappings

### Example 1: Post-deployment behavioral drift

If an incident record suggests:

- system passed launch criteria
- harmful behavior emerges later under real workload
- stale assurance or monitoring weakness is visible

Possible mapping:

- failure classes:
  - `F009` Validation-Lifecycle Break
  - `F007` Runtime Governance Substitution
- anti-patterns:
  - `AP014` Validation Freeze, Runtime Drift
  - `AP008` Evidence After Action
- constructive patterns:
  - `governance lifecycle validation`
  - `runtime evidence`
  - `coherence monitoring`

### Example 2: Agent credential or registration treated as accountability

If an incident record suggests:

- an agent or automated actor performed a consequential action
- technical traceability exists
- responsible principal binding remains weak

Possible mapping:

- failure classes:
  - `F008` Accountability Displacement
- anti-patterns:
  - `AP017` Agent Keys as Legal Personhood
  - `AP015` Framework Without Risk Profile
- constructive patterns:
  - `delegated agent identity`
  - `interface governance shape`
  - `normative charter`

### Example 3: Runtime action contradicts declared policy

If an incident record suggests:

- policy or oversight existed on paper
- runtime behavior still violated the declared rule
- evidence is mostly retrospective

Possible mapping:

- failure classes:
  - `F007` Runtime Governance Substitution
- anti-patterns:
  - `AP007` Policy PDF, Runtime Nothing
  - `AP009` Human Oversight as Ceremony
- constructive patterns:
  - `policy as runtime`
  - `runtime evidence`
  - `creation governance shape` or `interface governance shape` depending on
    where the break occurred

## Boundaries

This crosswalk should remain disciplined.

It is useful only if it stays:

- transparent about inference
- explicit about confidence
- modest about causality
- practical about mitigation
