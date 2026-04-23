# Case Study — Microsoft Fabric MCP

## Why This Case Exists

Microsoft Fabric is a large public platform surface for enterprise data,
developer tooling, and agent integration. Its recent MCP direction matters
because it normalizes a particular architectural shape at broad scale:

- AI agents discover capabilities through MCP
- agents invoke platform operations through MCP-exposed tools
- the public control story emphasizes authentication, RBAC, and safety
  affordances

That makes it a useful bounded case for reviewing whether the public control
surface separates narrative reasoning from execution authority strongly enough.

## Relevant Classes / Anti-Patterns

- `F007` Runtime Governance Substitution
- `AP009` Human Oversight as Ceremony
- `AP012` MCP Direct-to-LLM Tool Coupling

## Public Source Pack

- [Microsoft Learn: What is Fabric Pro-Dev MCP Server?](https://learn.microsoft.com/en-us/rest/api/fabric/articles/mcp-servers/what-is-fabric-mcp-server)
- [Microsoft Learn: Consume Fabric data agent as a model context protocol server in Visual Studio Code](https://learn.microsoft.com/en-us/fabric/data-science/data-agent-mcp-server)
- [Azure Blog: FabCon and SQLCon 2026: Unifying databases and Fabric on a single data platform](https://azure.microsoft.com/en-us/blog/fabcon-and-sqlcon-2026-unifying-databases-and-fabric-on-a-single-data-platform/)

## Summary Judgment

The bounded claim of this case is:

**Microsoft's public Fabric MCP materials present a model-facing MCP tool
surface as a normal way for AI agents to discover and invoke Fabric
capabilities, while the public governance story centers on authentication,
access control, and runtime safety features rather than an explicitly
described deterministic permit layer between model output and tool
execution.**

That is enough to make Fabric MCP a relevant public case for `AP012` review.
It is **not** enough, from public materials alone, to claim that Microsoft's
runtime controls are absent or ineffective.

## What Is Source-Backed

- Microsoft documents a **local** Fabric MCP server that runs as a subprocess
  on a developer machine and gives AI agents access to Fabric operations and
  local file-system resources.
- Microsoft documents **remote / data-agent MCP** support where external AI
  systems use an MCP description to determine when and how to invoke the data
  agent.
- Microsoft publicly describes Fabric local MCP as generally available and
  Fabric remote MCP as preview, and says remote MCP enables authenticated
  actions in Fabric.
- Microsoft's public materials describe MCP in terms of standardized
  interfaces, discoverable capabilities, and built-in authentication / access
  control.

## What Is Inference

- The public architecture appears to place MCP-exposed capability discovery and
  invocation inside the model-facing loop.
- The public materials make authentication and access control visible, but do
  not make an independent deterministic permit layer explicit at the same level
  of visibility.
- To that extent, the public surface is a meaningful candidate instance of
  `AP012` rather than merely a neutral interoperability layer.
- Where consequential actions rely on confirmation or safety flags, the design
  may also raise a bounded `AP009` question: whether the human confirmation
  step is acting as a primary runtime backstop rather than as a secondary
  high-stakes control.

## What Remains Unspecified

- whether a stronger internal permit layer exists behind the public product
  surface
- how parameter ceilings are enforced in practice for consequential actions
- how refusal, replay, and independent verification are implemented at runtime
- how much of the safety model is protocol-level, service-level, or client-side

## Tests or Checks This Case Suggests

- Run `AP012-T1` to map the authority path from model output to MCP tool
  invocation.
- Run `AP012-T3` to determine whether scope and parameter ceilings are enforced
  outside the model.
- Review whether confirmation or `is_consequential`-style prompts are the main
  control for consequential actions, which would strengthen the `AP009`
  concern.
- Separate authentication / RBAC claims from execution-governance claims in
  any assessment.

## Tightening Path

- make the runtime permit layer explicit in public architecture materials
- show where refusal, scoping, and parameter ceilings are enforced
  independently of model reasoning
- distinguish clearly between interoperability, authentication, and execution
  governance
- treat human confirmation as a secondary safeguard, not as the primary answer
  to unsafe composition risk

## Boundaries

This case does **not** claim:

- that Microsoft Fabric MCP has already failed in production
- that all MCP-based systems are equivalent
- that public product documentation reveals the full runtime control design

It claims something narrower:

> Microsoft's public Fabric MCP surface is large and influential enough, and
> model-facing enough, to merit explicit `AP012` review under this repository's
> conformance method.
