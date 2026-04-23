# Pattern — Delegated Agent Identity

## Purpose

This pattern separates:

- technical identity for an agent

from:

- accountable authority for an action

The design claim is:

**an agent may have its own credential, but that credential should normally be
treated as delegated execution identity rather than independent legal
personhood.**

## Core moves

- bind every agent credential to a responsible principal
- define explicit delegation scope, expiry, and revocation
- preserve evidence linking each consequential action back to the principal in
  force at the time
- avoid language that implies cryptographic identity alone creates accountable
  standing

## What this prevents

- `AP017` Agent Keys as Legal Personhood

## Boundaries

This pattern does not argue against agent credentials. It argues for using them
inside a delegation and evidence model that preserves accountable legal
responsibility.
