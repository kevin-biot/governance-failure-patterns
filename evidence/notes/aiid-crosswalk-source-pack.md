# AIID Crosswalk Source Pack

Checked on: 2026-04-23

## Purpose

This note records the public source basis for the repository's AI Incident
Database crosswalk work.

It exists to keep the boundary explicit between:

- what the AI Incident Database publishes directly
- what this repository infers as a governance interpretation
- what remains provisional until more detailed incident-by-incident mapping is
  performed

## Public Sources Used

### 1. AI Incident Database homepage

URL:
https://incidentdatabase.ai/

Why it matters:

- confirms the public role of AIID as an incident corpus
- confirms the general framing of the project

### 2. AI Incident Database taxonomy page

URL:
https://incidentdatabase.ai/taxonomies/

Why it matters:

- lists the public taxonomy families applied in AIID
- exposes the dimensions this repository is currently using as crosswalk inputs

Checked claims:

- AIID publicly lists taxonomies including:
  - `Center for Security and Emerging Technology (CSETv1)`
  - `Goals, Methods, and Failures (GMF)`
  - `MIT AI Risk Repository`
- public taxonomy dimensions visible on the page include items such as:
  - `Harm Distribution Basis`
  - `Sector of Deployment`
  - `Known AI Goal`
  - `Known AI Technology`
  - `Known AI Technical Failure`
  - `Risk Domain`
  - `Entity`
  - `Timing`
  - `Intent`

## What is source-backed

The following are treated as source-backed:

- AIID exists as a public incident database
- AIID exposes public taxonomy surfaces on its taxonomy page
- the listed taxonomy families and dimensions are available as public inputs to
  a governance crosswalk

## What is analytic inference

The following are this repository's interpretation, not AIID's own claim:

- that AIID can be usefully crosswalked into governance failure classes
- that dimensions like `Timing`, `Entity`, and `Known AI Technical Failure`
  currently provide the strongest bridge into this repository's taxonomy
- that dimensions like `Sector of Deployment`, `Intent`, and `Harm
  Distribution Basis` are only partially mapped today

## Editorial rule

The repository should not imply that AIID endorses the governance-failure
interpretation layer.

The correct relationship is:

- AIID provides incident records and taxonomy surfaces
- this repository overlays a governance interpretation

## Maintenance rule

If AIID changes its taxonomy surface:

- update the inventory and backlog note
- update the crosswalk method where necessary
- keep older mappings explicit about the taxonomy version or date checked
