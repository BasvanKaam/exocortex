---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [res, powerfuse, performance, terminal-server, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# PowerFuse performance shields (reference)

PowerFuse's performance management bundled several runtime controls for Terminal Servers:

- **Access Balancing**: capped the number of users starting a session on a machine concurrently, with per-machine exceptions.
- **SessionGuard**: enforced one session per user; a second attempt was queued with a message until the first session closed.
- **CPUShield**: lowered a process's priority to Idle when its CPU use stayed above a threshold (e.g. >70% for >3s), then restored priority once usage dropped (e.g. <10% for >30s). The Critical CPU Load Duration was tracked by PowerTrace.
- **MemoryShield**: optimized memory use of running processes and let more sessions be hosted per Terminal Server by capping physical memory per session and the number of running applications per session. When a cap was hit the user could not launch more apps until usage dropped.

Dated, product-specific reference.

*Bron: Core Knowledge doc 'Powerfuse Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [PowerFuse application, file, and IP security (reference)](powerfuse-application-and-file-security.md)
- [PowerFuse assignment model and tracing (reference)](powerfuse-assignment-model-and-tracing.md)
- [PowerFuse Instant LogOff (reference)](powerfuse-instant-logoff.md)
- [RES PowerFuse / Workspace Manager (reference)](res-powerfuse-workspace-manager-overview.md)
- [How memory works in Terminal Server: shared executables](terminal-server-memory-shared-executables.md)
