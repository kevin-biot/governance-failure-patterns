# Pattern — Reference Governance Shapes

## Purpose

This note adds the positive side of the repository.

The repo should not only name governance failures. It should also show the
recurring structural shapes that appear in more serious governance designs.

These are not the one true architecture. They are non-normative reference
surfaces that help answer:

> what does governance often look like when it is structurally real?

## Six recurring surfaces

1. `Creation`
   Governed objects are born with authority, scope, policy baseline, and
   refusal paths.

2. `Data`
   Data carries governance metadata that survives storage, access, and
   movement.

3. `Execution`
   Runtime type, admission, dependency, and attestation are policy-bound.

4. `Interface`
   APIs expose delegated scope, refusal semantics, and evidence hooks.

5. `Evidence`
   Actions become replayable governance evidence rather than descriptive logs.

6. `Portability`
   Governance survives migration and exit, not only steady-state operation.

## Why this matters

Without positive shapes, governance work risks becoming a catalogue of
critique.

With them, the repository can say something more useful:

**governance is a binding structure around action, not a commentary layer after
action.**

## Related notes

- [creation-governance-shape.md](./creation-governance-shape.md)
- [data-governance-shape.md](./data-governance-shape.md)
- [execution-governance-shape.md](./execution-governance-shape.md)
- [interface-governance-shape.md](./interface-governance-shape.md)
- [evidence-governance-shape.md](./evidence-governance-shape.md)
- [portability-governance-shape.md](./portability-governance-shape.md)

## Boundaries

These shapes do not prescribe one stack, one vendor, or one protocol.

They are useful because they remain architectural and governance-oriented:

- what must be bound
- where refusal belongs
- what evidence is needed
- how governance survives lifecycle change
