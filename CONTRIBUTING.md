# Contributing to Signal Gating Protocol

Choose the smallest path that fits the change.

## Questions and early ideas

Use [GitHub Discussions](https://github.com/orgs/signalgatingprotocol/discussions)
for questions, design exploration, and prior art.

## Implementation changes

Open an issue or pull request in the affected SDK repository. For the Python
reference implementation, use
[`signalgatingprotocol/python-sdk`](https://github.com/signalgatingprotocol/python-sdk).
Follow that repository's build, test, lint, and type-check commands.

## Protocol changes

Changes to Signal, Gate, Agent, Mesh, wire behavior, versioning, or conformance
go through the [`community` RFC process](https://github.com/signalgatingprotocol/community/tree/main/rfcs).

## Pull requests

- Keep one coherent change per pull request.
- Explain the behavior before and after the change.
- Add or update tests for executable behavior.
- Update public documentation when a user-facing contract changes.
- Link the issue, discussion, or RFC that establishes the reason for the work.
- Do not include credentials, private data, generated caches, or unrelated edits.

By contributing, you agree that your contribution is licensed under the license
of the repository receiving it.
