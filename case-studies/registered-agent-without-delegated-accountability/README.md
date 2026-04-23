# Case Study — Registered Agent Without Delegated Accountability

## Why This Case Exists

This case captures a recurring governance pattern in emerging agentic commerce
and payment designs:

- the framework claims a "registered," "trusted," or "traceable" agent
- the agent may have a technical credential or tokenized identity
- but the accountable delegation chain to a legal principal remains weak,
  underspecified, or invisible

The problem is not registration by itself. The problem is mistaking technical
registration for a complete accountability model.

## Relevant Anti-Patterns

- `AP015` Framework Without Risk Profile
- `AP016` Governance Without Lifecycle Validation
- `AP017` Agent Keys as Legal Personhood

## Summary Judgment

The bounded claim of this case is:

**agent registration, traceability, or technical identity does not by itself
solve authority provenance, accountable delegation, or dispute traceability.**

That gap matters most in payment and commerce settings where a later dispute
forum needs to answer:

- who authorised the action
- under what delegation
- with what scope
- on whose behalf
- and who remains accountable when the agent acted

## Pattern Shape

The recurring market narrative looks like this:

- only registered agents may transact
- trusted agents are authenticated or tokenized
- transactions become visible and traceable
- consumers or businesses retain control

Those claims may all be directionally useful. But they still leave open the
harder governance questions:

- what binds the agent credential to a responsible principal?
- what delegation scope was in force?
- what are the expiry and revocation rules?
- does a dispute trace stop at the agent token, or reach the legal actor?
- who measures runtime drift once the agent operates under real workload?

## What This Case Asks Reviewers To Check

1. **Registration versus authority**
   Is the agent merely registered, or is its authority explicitly delegated and
   bounded?

2. **Traceability versus accountability**
   Can a transaction be traced technically, and can it also be attributed to a
   responsible legal actor?

3. **Consent versus operating control**
   Is user or business consent defined only at setup time, or is it preserved
   through revocation, expiry, and runtime intervention?

4. **Identity versus standing**
   Does the design implicitly treat technical identity as if it created legal
   standing?

## Why This Is a Governance Pattern Rather Than a Vendor Critique

This case does not depend on one company, one product, or one standard.

It is a reusable pattern because the same structure can appear whenever
agentic-payment or agentic-commerce systems promise:

- trusted agents
- registered agents
- traceable agents
- consented agent purchasing

without making delegated accountability equally explicit.

## Tightening Path

- treat agent credentials as delegated execution identity
- bind them to accountable principals and bounded scope
- define revocation, expiry, and dispute evidence clearly
- require runtime monitoring once the agent moves from registration into live
  operation

## Boundaries

This case does **not** claim that agent registration is useless.

It claims something narrower:

> registration and traceability are only partial controls unless they are joined
> to delegated authority, accountable principal binding, and dispute-grade
> evidence
