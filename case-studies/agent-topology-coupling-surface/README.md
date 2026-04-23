# Case Study — Agent-Agent Topology as a Coupling Surface

## Why This Case Exists

This case captures a stronger claim than the baseline `agent-chains` case:
some architectures do not merely *permit* natural-language peer coupling, they
make it the default substrate through which every consequential handoff flows.

The governance question is therefore not only "can coupled collapse happen?"
but also "did the architecture make coupling saturation inevitable at deploy
time?"

## Relevant Classes

- `F003` Entrained Consensus Mistaken for Validation
- `F004` Coupled Reasoning Collapse
- `F005` Stationarity Fiction in State Models

## Provenance Boundary

This note is intentionally split across two evidence levels:

- public evidence, which supports the existence of the broader risk family
- private internal research, which currently supports the stronger
  cross-topology claim

The provenance note is tracked in
[../../evidence/notes/agent-topology-coupling-surface-provenance.md](../../evidence/notes/agent-topology-coupling-surface-provenance.md).

## Summary Judgment

The bounded thesis of this case is:

**agent-agent natural-language coupling is not only a runtime behavior. It can
also be a topology property set at deploy time.**

That means some architectures should be treated as living on a pre-selected
coupling surface before any specific workload is applied.

## What the Public Evidence Supports

The public Sentinel material already supports a meaningful governance claim:

- multi-agent LLM systems can exhibit triggered collapse rather than smooth
  degradation
- probe success can dissociate from behavioral health
- internal agreement cannot be assumed to represent independent validation
- monitoring effects can be model-dependent

This is enough to treat natural-language peer coupling as a genuine governance
risk family.

See the related case note:
[../agent-chains/README.md](../agent-chains/README.md).

## What the Private Internal Research Adds

Private internal cross-topology measurement work suggests a stronger claim:

- architectures with typed or schema-bounded inter-agent coordination can sit
  near a structurally low coupling regime
- architectures where every inter-agent handoff is natural-language mediated
  can sit near a structurally saturated coupling regime
- workload perturbations may move local behavior while leaving the deeper
  substrate position largely determined by topology

This repository is not yet publishing the underlying private measurement corpus
or implementation details behind that stronger claim.

## Governance Interpretation

If the stronger topology claim continues to hold, then the design mistake is
not merely "we failed to monitor drift." It is:

- selecting an architecture that manufactures a large coupling surface by
  default
- then treating downstream monitoring or agent consensus as if they can recover
  independence that the topology already destroyed

In that frame, topology choice becomes a governance decision rather than a
neutral implementation detail.

## Anti-Pattern Linkage

This case strengthens:

- `AP006` Natural-Language Peer Coupling

It suggests the anti-pattern should often be read architecturally:

> if every peer edge is natural language, then coupling is not an accidental
> failure mode. It is a built-in property of the design.

## Bounded Tightening Path

A constructive response is available:

- prefer typed or schema-bounded inter-agent contracts for consequential paths
- keep deterministic control state separate from narrative exchange
- treat free-form peer language as an exception surface, not the default
  substrate
- require stronger justification before adopting architectures whose safety
  story depends on post hoc monitoring of a saturated coupling surface

## Boundaries

This case does **not** claim:

- that every multi-agent architecture is equally fragile
- that all natural-language handoffs are always unacceptable
- that the stronger topology claim is already fully established by public
  evidence alone

It claims something narrower:

> public evidence establishes the risk family; private internal research
> currently suggests that topology may determine the coupling surface more
> strongly than workload does
