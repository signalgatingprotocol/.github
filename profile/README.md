# Signal Gating Protocol

<p align="center">
  <img src="assets/cropped.png" alt="SGP Logo" />
</p>

<p align="center">
  <strong> A default‑deny routing + context provenance for agent graphs.</strong>
</p>

<p align="center">
  <a href="https://signalgatingprotocol.github.io">Documentation</a> |
  <a href="https://signalgatingprotocol.github.io/specification">Specification</a> |
  <a href="https://github.com/orgs/signalgatingprotocol/discussions">Discussions</a>
</p>

**Signal Gating Protocol (SGP) is:** a control-plane protocol for agent graphs that standardizes:

1. what “processors” are and how they declare activation conditions
2. what “signals” are and how they carry features + provenance
3. how an executive router produces a GatePlan (explicit activation + suppression)
4. how runtimes enforce context minimization (each processor sees only what it needs)
5. how executions emit a Receipt for audit + learning

**What SGP is not:** not a tool protocol (that’s MCP), not agent chat (that’s A2A), not commerce (that’s UCP). SGP is the missing executive function layer.

## Getting Started

- 📚 Read the [Documentation](https://signalgatingprotocol.github.io) for guides and tutorials
- 🔍 Review the [Specification](https://signalgatingprotocol.github.io/specification) for protocol details
- 💻 Use our SDKs to start building:
  - [python-sdk](https://github.com/signalgatingprotocol/python-sdk)
