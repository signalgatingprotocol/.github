<p align="center">
  <img src="assets/light.png" alt="Signal Gating Protocol" width="640" />
</p>

<h3 align="center">Typed, gated, observable signal flow for multi-agent systems.</h3>

<p align="center">
  <a href="https://signalgatingprotocol.github.io">Documentation</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/signalgatingprotocol/python-sdk">Python SDK</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/signalgatingprotocol/community">Community</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/orgs/signalgatingprotocol/discussions">Discussions</a>
</p>

## Why SGP

Agent graphs often forward too much context, hide routing policy in application
code, and make execution difficult to reconstruct. SGP makes those control
decisions explicit with typed signals, composable gates, autonomous processors,
and observable mesh topology.

## Current model

| Primitive | Responsibility |
| --- | --- |
| **Signal** | Typed, immutable event with identity, lineage, priority, and metadata. |
| **Gate** | Composable policy that admits, drops, transforms, or controls signal flow. |
| **Agent** | Asynchronous signal processor with typed handlers, lifecycle, request and response, and tools. |
| **Mesh** | Directed agent topology with gated edges and coordination patterns. |

The [Python SDK](https://github.com/signalgatingprotocol/python-sdk) is the
reference implementation.

## Maturity

| Surface | Status |
| --- | --- |
| Signal, Gate, Agent, and Mesh runtime | Implemented in the alpha Python SDK |
| JSON signal wire envelope and trajectory receipts | Implemented in the alpha Python SDK |
| Cross-runtime interoperability and conformance suite | Draft |
| GatePlan and default-deny control plane | Design stage |

The implementation is usable for experiments, but the protocol and public API
may change before 1.0.

## Try it

```bash
pip install "signal-gating @ git+https://github.com/signalgatingprotocol/python-sdk"
```

```python
import asyncio
from signal_gating import Agent, Gate, Mesh, Signal

class Task(Signal):
    text: str

producer = Agent("producer")
worker = Agent("worker", gates=[Gate.by_priority(3)])

@worker.on(Task)
async def handle(task: Task):
    print(task.text)

mesh = Mesh([producer, worker])
mesh.connect(producer, worker)

async def main():
    async with mesh:
        await producer.emit(Task(text="admitted", priority=5))
        await producer.emit(Task(text="dropped", priority=1))

asyncio.run(main())
```

## Participate

- Read the [documentation](https://signalgatingprotocol.github.io) and current
  [draft specification](https://signalgatingprotocol.github.io/specification/).
- Ask questions or challenge the model in
  [Discussions](https://github.com/orgs/signalgatingprotocol/discussions).
- Propose protocol changes through the
  [RFC process](https://github.com/signalgatingprotocol/community/tree/main/rfcs).
- Report vulnerabilities through the private process in
  [SECURITY.md](https://github.com/signalgatingprotocol/.github/blob/main/SECURITY.md).

SGP is alpha. Precise criticism, implementations, and failure cases are welcome.
