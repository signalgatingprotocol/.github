# Security policy

## Report privately

Do not open a public issue for a suspected vulnerability.

Use GitHub's private vulnerability reporting in the affected repository. If the
affected repository does not expose private reporting, use the
[`community` security advisory form](https://github.com/signalgatingprotocol/community/security/advisories/new)
and identify the affected repository in the report.

Include:

- affected version, tag, or commit;
- impact and affected trust boundary;
- minimal reproduction steps or proof of concept;
- known mitigations;
- whether the issue is already public or actively exploited.

Maintainers will coordinate disclosure through the private advisory. Active
exploitation or a public exploit may require accelerated mitigation and
communication.

## Supported versions

Until stable releases exist, security fixes target the latest default branch.
After tagged releases begin, this file will list the supported release lines.

## Scope

Security-sensitive behavior includes unauthorized signal delivery, gate bypass,
wire-format confusion, unsafe deserialization, forged or corrupted trajectory
data, cross-agent data exposure, denial of service, and dependency compromise.

Design concerns about features that are not implemented are not vulnerabilities.
Raise those through the public RFC process unless disclosure would reveal an
exploitable weakness in current code.
