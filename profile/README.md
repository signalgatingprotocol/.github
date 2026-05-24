<p align="center">
  <img src="assets/light.png" alt="Signal Gating Protocol" width="640" />
</p>

<h3 align="center">Agent-native signal orchestration for autonomous AI systems.</h3>

<p align="center">
  <a href="https://signalgatingprotocol.github.io">Docs</a>
  &nbsp;·&nbsp;
  <a href="https://signalgatingprotocol.github.io/specification">Spec</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/orgs/signalgatingprotocol/discussions">Discussions</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/signalgatingprotocol/python-sdk">Python SDK</a>
</p>

---

## Why

Every agent sees everything. Context windows fill with noise, stale information crowds out what matters, and one agent's hallucination cascades through the rest.

The bottleneck for multi-agent systems is not models, tools, or memory. It is **executive control**: a structural layer that decides which signals reach which agent, and wires agents into coordinated workflows.

SGP is that layer: typed signals, composable gates, autonomous agents, and meshes. Controlled, observable signal flow between agents.

## The primitives

| | |
|---|---|
| **Signal** | A typed, immutable event. Carries a priority and metadata, derived rather than mutated. |
| **Gate** | A composable predicate that controls which signals reach an agent. Chain, or, and, invert. |
| **Agent** | An autonomous signal processor (typed handlers, lifecycle, request/response, and tools). Where a runtime like Hermes plugs in. |
| **Mesh** | The agent network: `connect` agents, then coordinate with scatter, map/reduce, workflow, and race. |

The reference implementation is the [Python SDK](https://github.com/signalgatingprotocol/python-sdk).

## What SGP is not

- **Not a tool protocol**: that is MCP.
- **Not agent chat**: that is A2A.
- **Not commerce**: that is UCP.

SGP is orthogonal. The missing executive function.

## Roadmap

A control plane on top of the primitives: an explicit router that emits a **GatePlan** (who activates, with what context), a **Runtime** that enforces it default-deny, and **Receipts**, verifiable records of every execution, for audit and learning. Design-stage; the four primitives above are what ships today.

## Start

- [Documentation](https://signalgatingprotocol.github.io): guides and concepts
- [Specification](https://signalgatingprotocol.github.io/specification): the protocol surface
- [python-sdk](https://github.com/signalgatingprotocol/python-sdk): reference implementation
- [Discussions](https://github.com/orgs/signalgatingprotocol/discussions): questions, critique, prior art

## Status

Draft. The protocol surface is still moving. Critique welcome.
