<p align="center">
  <img src="assets/light.png" alt="Signal Gating Protocol" width="640" />
</p>

<h3 align="center">The executive function layer for agent graphs.</h3>

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

Every agent sees everything. Every retrieval is best-effort. Every execution is unverifiable.

The bottleneck for agent systems is not models, tools, or memory. It is **executive control** — a layer that decides what runs, what context it sees, and produces proof of what happened.

SGP is that layer. Default-deny. Provenance-aware. Receipt-backed.

## The protocol

Five primitives. Nothing more.

| | |
|---|---|
| **Processor** | A unit of agent work that declares its activation conditions. |
| **Signal** | A typed feature with provenance — what is true, and how we know it. |
| **GatePlan** | The router's explicit decision: who activates, who is suppressed, and with what input. |
| **Receipt** | A verifiable record of every execution — for audit and learning. |
| **Runtime** | Enforces the plan. Each processor receives only the context it declared. |

The router is the executive. The runtime is the enforcer. The rest is application.

## What SGP is not

- **Not a tool protocol** — that is MCP.
- **Not agent chat** — that is A2A.
- **Not commerce** — that is UCP.

SGP is orthogonal. The missing executive function.

## Start

- [Documentation](https://signalgatingprotocol.github.io) — guides and concepts
- [Specification](https://signalgatingprotocol.github.io/specification) — the protocol surface
- [python-sdk](https://github.com/signalgatingprotocol/python-sdk) — reference implementation
- [Discussions](https://github.com/orgs/signalgatingprotocol/discussions) — questions, critique, prior art

## Status

Draft. The protocol surface is still moving. Critique welcome.
