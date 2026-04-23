# AI Incident Database — Taxonomy Inventory and Mapping Backlog

## Purpose

This note turns the AIID crosswalk from a one-off method into a maintained work
surface.

Its role is to:

- list the external AI Incident Database taxonomy surfaces relevant to this
  repository
- state what is already mappable into governance-failure-patterns
- identify what remains only partially mapped
- identify where new patterns or classes may be needed

## Source basis

Primary public source:

- [AI Incident Database taxonomy list](https://incidentdatabase.ai/taxonomies/)

As of 2026-04-23, AIID publicly lists at least these applied taxonomies:

- `Center for Security and Emerging Technology (CSETv1)`
- `Goals, Methods, and Failures (GMF)`
- `MIT AI Risk Repository`

## Status labels

Use these labels in the backlog:

- `mapped`
  A clear governance interpretation path already exists in this repository.
- `partially_mapped`
  Some governance interpretation is available, but the fit is incomplete.
- `unmapped`
  No clean governance mapping exists yet.
- `needs_new_pattern`
  The external taxonomy surface is useful, but the repository likely needs a
  new failure class, anti-pattern, or constructive pattern.

## Inventory

| External taxonomy family | External dimension | Why it matters | Likely governance-failure relevance | Current status | Notes |
|---|---|---|---|---|---|
| CSETv1 | Harm Distribution Basis | Describes how harm lands across affected parties | Can help distinguish accountability, risk-profile, and governance-scope issues | `partially_mapped` | Harm alone does not determine the governance mechanism |
| CSETv1 | Sector of Deployment | Indicates deployment context | Can refine risk-profile and lifecycle expectations | `partially_mapped` | Better for domain overlays than direct anti-pattern mapping |
| GMF | Known AI Goal | Captures what the system was trying to do | Useful for separating intended function from governance failure | `partially_mapped` | Often contextual rather than dispositive |
| GMF | Known AI Technology | Captures the technical substrate | Helps identify likely governance surfaces such as state models, agent coupling, or tool use | `partially_mapped` | Should not be treated as governance by itself |
| GMF | Known AI Technical Failure | Captures the immediate technical failure mode | Often the strongest bridge to governance interpretation | `mapped` | Especially useful for lifecycle, drift, control, and evidence failures |
| MIT AI Risk Repository | Risk Domain | High-level incident/risk domain classification | Useful for triage, but not sufficient by itself for governance diagnosis | `partially_mapped` | Good as an entry point, weak as a final governance label |
| MIT AI Risk Repository | Entity | Helps distinguish human, AI, or mixed responsibility surfaces | Useful for accountability and delegated-authority questions | `mapped` | Strong relevance to accountability displacement |
| MIT AI Risk Repository | Timing | Distinguishes pre-deployment and post-deployment dynamics | Strong bridge to lifecycle validation and runtime governance | `mapped` | One of the clearest governance-relevant dimensions |
| MIT AI Risk Repository | Intent | Distinguishes intentional vs unintentional risk | Useful for separating malicious use from governance weakness | `partially_mapped` | Helps avoid over-reading every incident as the same failure class |

## Current strongest mappings

The cleanest current bridges appear to be:

### 1. Timing -> lifecycle and runtime governance

Especially for:

- post-deployment incidents
- stale validation stories
- live drift under real workload

Strong internal targets:

- `F009` Validation-Lifecycle Break
- `F007` Runtime Governance Substitution
- `AP014` Validation Freeze, Runtime Drift
- `AP008` Evidence After Action

### 2. Entity -> accountability and delegated authority

Especially where:

- technical action is visible
- accountable principal binding is weak

Strong internal targets:

- `F008` Accountability Displacement
- `AP017` Agent Keys as Legal Personhood
- `AP015` Framework Without Risk Profile

### 3. Known AI Technical Failure -> governance-structure interpretation

Especially where the public failure mode points toward:

- weak runtime control
- post-hoc evidence
- state-model drift
- agent coupling
- inadequate scope or permit boundaries

Strong internal targets:

- `AP005`
- `AP006`
- `AP012`
- `AP013`
- `AP014`

## Current weaker mappings

The hardest AIID dimensions to map cleanly today are:

### Harm Distribution Basis

Why weaker:

- harm distribution helps describe who was affected
- it does not by itself identify the governance design weakness

Needed:

- more explicit governance patterns for burden distribution and protected
  stakeholder handling

### Sector of Deployment

Why weaker:

- sector matters for consequence and expected control rigor
- but the repository currently has only limited sector-specific overlays

Needed:

- optional domain overlays for finance, health, public-sector, and critical
  infrastructure settings

### Intent

Why weaker:

- intent helps distinguish threat posture
- but the repository is stronger on governance structure than on adversary
  classification

Needed:

- possibly a future pattern family on adversarial governance failure versus
  operational governance failure

## Backlog candidates

### Candidate mapping workstream A

Map AIID `Timing` systematically into:

- lifecycle break
- runtime substitution
- stale validation
- operating-envelope departure

### Candidate mapping workstream B

Map AIID `Entity` systematically into:

- delegated accountability
- human oversight realism
- credential versus principal distinction

### Candidate mapping workstream C

Map `Known AI Technical Failure` into:

- state-model misuse
- agent-coupling risks
- tool-authority coupling
- evidence/control separation failures

### Candidate mapping workstream D

Create domain overlays so `Sector of Deployment` becomes more useful in the
governance layer.

### Candidate mapping workstream E

Add burden-distribution and stakeholder-protection patterns so `Harm
Distribution Basis` can be crosswalked more meaningfully.

## Maintenance rule

This inventory should evolve when:

- AIID adds or changes taxonomy surfaces
- this repository adds new failure classes or anti-patterns
- mapping work reveals a repeated gap that deserves a new constructive pattern

## Working principle

The goal is not total coverage immediately.

The goal is to make the mapping backlog explicit, so future work can grow in a
disciplined way rather than as scattered examples.
