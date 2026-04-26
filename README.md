# Governance Failure Patterns

*A public-interest taxonomy and conformance method for recurring governance
failures in AI-assisted decision systems, policy tooling, and agentic
infrastructure.*

This repository names a class of problems that are often discussed only as
isolated incidents or vendor-specific complaints:

- governance that looks stronger than it is
- frameworks that describe control without binding runtime behavior
- agentic and policy systems that accumulate hidden fragility behind trust,
  safety, or compliance language

The repository is designed to make those failures:

- **legible** as named classes
- **challengeable** through conformance tests
- **repairable** through explicit mitigation patterns

## What this repository contains

- [framework.md](./framework.md)
  What a governance failure pattern is, and how the repository distinguishes
  failure classes from anti-patterns.
- [taxonomy/](./taxonomy/)
  Deeper recurrent failure classes such as formal transparency without
  foundational adequacy, runtime governance substitution, accountability
  displacement, and validation-lifecycle break.
- [anti-patterns/](./anti-patterns/)
  Deployer-visible bad habits and architectural moves that instantiate or
  amplify those deeper failures.
- [case-studies/](./case-studies/)
  Bounded analyses of public or generalized governance patterns.
- [patterns/](./patterns/)
  Repair-oriented notes such as `policy as runtime`, `runtime evidence`,
  `doctrine as coupling layer`, `sovereignty requires verifier-friendly
  evidence`, `reference governance shapes`, `governance lifecycle validation`,
  and `delegated agent identity`.
- [spec/](./spec/)
  Profile schema, anti-pattern conformance tests, attestation format, and
  worked examples.
- [docs/](./docs/)
  Longer-form method notes and crosswalks, including the AI Incident Database
  governance crosswalk method, mapping guidance, taxonomy inventory, and OECD
  mitigation-side crosswalk notes.
- [templates/](./templates/) and [reports/templates/](./reports/templates/)
  Reusable authoring scaffolds for cases, patterns, profiles, and findings
  reports.
- [evidence/](./evidence/)
  Source-pack and provenance notes that keep the boundary clear between
  source-backed claims, analytic inference, and non-public supporting work.

## Why this exists

Current markets for AI governance, agent safety, and policy assurance are full
of performative assertions:

- “registered” agents
- “trusted” agents
- “human in the loop”
- “safe because sandboxed”
- “governed because logged”
- “validated because tested before launch”

Those claims are not always false, but they are often incomplete in ways that
matter operationally, institutionally, and legally.

This repository argues that the right response is not only critique. It is a
better method:

1. name the failure class
2. name the visible anti-pattern
3. define the conformance tests
4. state the evidence level honestly
5. offer a bounded demotion or repair path

## Public-interest reuse potential

This repository is published openly as public-interest scaffolding. The goal is
to shorten the path from vague governance language to concrete institutional
artifacts by giving regulators, standards bodies, deployers, auditors, and
reviewers a named set of failure classes, anti-patterns, and repair patterns
they can reuse directly.

In particular, the material here is intended to be reusable as input to:

- harmonised standards discussions and draft review
- European Commission guidance
- common specifications where standards are late or insufficient
- AI regulatory sandbox methods, reporting, and evidence-based learning
- conformity assessment and audit practice
- deployer governance and remediation programs

The repository does **not** claim to be an official standard, guidance
document, or conformity assessment artifact in itself. It is an open diagnosis
and remediation scaffold that institutions with formal mandates can refine and
formalise.

This repository is especially useful when paired with
[Blast Radius Framework](https://github.com/kevin-biot/blast-radius-framework),
which provides the positive rating, attestation, and operational-impact layer
that complements the failure taxonomy here.

## Companion repository

This repository is a companion to
[Blast Radius Framework](https://github.com/kevin-biot/blast-radius-framework).

The relationship is:

- **Blast Radius Framework** rates the operational blast surface of a deployed
  system and provides an attestation form.
- **Governance Failure Patterns** diagnoses the governance weakness patterns
  that often explain why systems are weakly controlled, misleadingly governed,
  or difficult to audit.

See [docs/blast-radius-framework-relationship.md](./docs/blast-radius-framework-relationship.md)
for the fuller distinction.

## Current taxonomy

The current seed classes are:

- `F001` Formal Transparency Without Foundational Adequacy
- `F002` Absorbed Drift and Baseline Laundering
- `F003` Entrained Consensus Mistaken for Validation
- `F004` Coupled Reasoning Collapse
- `F005` Stationarity Fiction in State Models
- `F006` Rulebook Without Doctrine
- `F007` Runtime Governance Substitution
- `F008` Accountability Displacement
- `F009` Validation-Lifecycle Break
- `F010` Risk-Profile Omission

The current anti-pattern catalogue includes, among others:

- `AP007` Policy PDF, Runtime Nothing
- `AP008` Evidence After Action
- `AP009` Human Oversight as Ceremony
- `AP010` Capability Discovery as Attack Surface
- `AP012` MCP Direct-to-LLM Tool Coupling
- `AP013` Sandbox Equals Safety
- `AP014` Validation Freeze, Runtime Drift
- `AP015` Framework Without Risk Profile
- `AP016` Governance Without Lifecycle Validation
- `AP017` Agent Keys as Legal Personhood

## How to use it

### As a researcher or critic

- use the taxonomy to classify recurrent governance failures
- use the case-study and provenance templates to keep claims bounded
- distinguish clearly between public evidence, analytic inference, and any
  non-public supporting basis
- use [docs/aiid-governance-crosswalk-method.md](./docs/aiid-governance-crosswalk-method.md)
  when mapping public AI incident records into governance interpretations
- use [docs/aiid-taxonomy-inventory-and-mapping-backlog.md](./docs/aiid-taxonomy-inventory-and-mapping-backlog.md)
  to track which external taxonomy surfaces are already mapped and which still
  need deeper governance work
- use [docs/oecd-tool-catalogue-crosswalk-method.md](./docs/oecd-tool-catalogue-crosswalk-method.md)
  to connect governance failure patterns to public mitigation and assurance
  tool categories

### As a deployer or assessor

- identify which anti-patterns are in scope
- populate a profile using [spec/gf-profile.schema.json](./spec/gf-profile.schema.json)
- run the relevant procedures in
  [spec/anti-pattern-conformance-tests.md](./spec/anti-pattern-conformance-tests.md)
- produce findings using the templates in [reports/templates/](./reports/templates/)

### As a policymaker, standards body, or reviewer

- use the repository as a negative reference
- challenge frameworks and products that claim governance without concrete risk
  profiles, lifecycle validation, delegated accountability, or runtime control

## Editorial standard

This repository is intended for public use. Documents should be:

- class-first, not enemy-first
- bounded, not totalizing
- evidence-aware, not rhetorical
- repair-oriented, not merely oppositional

See [editorial-policy.md](./editorial-policy.md).

## Release discipline

Structural changes should move through explicit change control rather than
informal drift.

- [CHANGELOG.md](./CHANGELOG.md)
  Records structural additions and meaningful claim-shape changes.
- [CONTRIBUTING.md](./CONTRIBUTING.md)
  Defines contribution priorities, claim classes, and versioning rules.
- [PUBLICATION-STANDARD.md](./PUBLICATION-STANDARD.md)
  Defines the public-readiness gates for publishing notes, classes, and cases.

The current baseline release tag is `v0.1.0`.

## Status

The repository is published as a baseline public framework and will continue to
evolve through tagged releases and documented structural changes.

The publication standard is straightforward:

- non-public or proprietary implementation detail removed or generalized
- claims kept bounded and falsifiable
- at least one mitigation or tightening path stated

## Contributing

The most useful contributions are:

- new failure classes with clear boundaries
- anti-patterns tied to real conformance questions
- worked profiles and example assessments
- critiques that improve falsifiability, evidence discipline, or repair paths

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the contribution standard and
[PUBLICATION-STANDARD.md](./PUBLICATION-STANDARD.md) for public-release gates.

## License

The text of this repository is licensed under
[Creative Commons Attribution 4.0 International (CC-BY-4.0)](./LICENSE).

Unless stated otherwise, examples, templates, and prose may be copied,
adapted, and reused under that license.
