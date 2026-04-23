# AIID Governance Crosswalk — Starter Mapping Matrix

## Purpose

This matrix provides a quick-start bridge from common public incident signals to
plausible governance interpretations.

It is intentionally suggestive rather than definitive.

## Matrix

| Public incident signal | Likely failure classes | Likely anti-patterns | Candidate constructive patterns |
|---|---|---|---|
| System passed testing but harmful behavior emerged later under live workload | `F009`, `F007` | `AP014`, `AP008` | `governance lifecycle validation`, `runtime evidence`, `coherence monitoring` |
| Policy existed on paper but runtime behavior violated it | `F007` | `AP007`, `AP009` | `policy as runtime`, `runtime evidence`, `interface governance shape` |
| Logging exists but mainly after the consequential action | `F007` | `AP008` | `runtime evidence`, `evidence governance shape` |
| Technical registration or credential is visible, but accountability to a responsible principal is weak | `F008`, `F010` | `AP017`, `AP015` | `delegated agent identity`, `normative charter`, `interface governance shape` |
| Agent-to-agent or model-mediated coordination appears to have amplified failure | `F003`, `F004` | `AP006`, `AP012` | `bounded AI role`, `deterministic measurement substrate`, `coherence monitoring` |
| State model or monitoring surface looked stable while the underlying regime changed | `F002`, `F005` | `AP005`, `AP014` | `deterministic measurement substrate`, `coherence monitoring`, `governance lifecycle validation` |
| System was described as safe because of sandboxing or technical containment alone | `F007`, `F010` | `AP013`, `AP015` | `risk profiling`, `execution governance shape`, `runtime evidence` |
| Migration, handoff, or cross-system transfer caused governance guarantees to weaken or disappear | `F010`, `F009` | `AP015`, `AP016` | `portability governance shape`, `governance lifecycle validation` |

## How to use this matrix

- start from the public incident signal
- treat the row as a hypothesis generator
- validate against the actual incident text
- record ambiguity instead of forcing a fit

## Boundaries

This matrix is not a scoring engine.

It is a starter lens for analysts doing first-pass governance interpretation.
