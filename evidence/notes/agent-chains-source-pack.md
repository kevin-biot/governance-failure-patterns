# Agent Chains / Sentinel Source Pack

Checked on: 2026-04-23

## Purpose

This note records the public source pack used for the `agent-chains` case study
and the boundary between source-backed claims and local analytic synthesis.

## Public Sources Used

### 1. Sentinel public repository

URL:
https://github.com/jasongagne-git/sentinel

Why it matters:

- public-facing summary of the Sentinel framework
- public-facing summary of the key findings
- public statement of experiment scale and design

Checked claims:

- Sentinel is presented as an empirical research framework for behavioral drift
  in multi-agent LLM systems
- multi-party conversation over hundreds of turns
- calibrated baselines and dual-probe methodology
- 40+ experiments and 20,000+ messages
- 0/12 baseline runs collapse
- 5/6 mutation-fork runs collapse at a deterministic turn
- pre-collapse thinning gradient
- three post-collapse modes
- probe-conversation dissociation
- hollow verbosity
- model-dependent observer effects

Verification note:

- repository README checked directly on 2026-04-23
- no public paper URL beyond the repository's own "preprint forthcoming"
  statement is relied on in the current case note

## Non-Public Drafting Substrates

These informed the local analytic structure but are not the public evidence
base for the current case note:

- DOP governance note on agent chains as an antipattern in high-risk domains
- DOP governance note on the Gagne collapse analogy for policy framing

## Maintenance Rule

If this case study expands, keep the same boundary explicit:

- what the public Sentinel material states
- what this repository infers from those findings
- what remains analogy rather than direct empirical claim
