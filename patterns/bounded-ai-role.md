# Pattern — Bounded AI Role

## Purpose

AI should have an explicitly bounded role in governance-relevant systems rather
than becoming hidden authority by convenience.

## Core moves

- define what the AI layer may do
- define what it may not do
- keep consequential authority outside unconstrained model behavior
- require provenance and review around AI-generated governance inputs

## What this prevents

- hidden delegation of authority to a fluent model layer
- policy drift through unversioned prompts or generated rationale
- weaker forms of `AP012` MCP Direct-to-LLM Tool Coupling

## Minimal artefacts

- allowed task classes
- prohibited task classes
- handoff rule to deterministic or human-controlled layers
- versioning and review rule for AI outputs used in governance

## Working question

What exactly is the AI allowed to decide, and what must remain outside its
authority?

## Boundaries

Bounding the AI role does not mean banning AI. It means keeping assistance from
quietly turning into authority.
