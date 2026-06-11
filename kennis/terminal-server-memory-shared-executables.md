---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [terminal-server, memory, working-set, committed-memory, shared-executables]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# How memory works in Terminal Server: shared executables

Each user running an app on a Terminal Server uses memory for it as on a normal workstation, plus ~4MB per-session overhead, on top of the base OS (~128MB in that era). But naive per-user multiplication overstates real usage for two reasons:

1. Apps use varying amounts of memory depending on what they have open, and supporting DLLs can dominate.
2. **Windows shares a single copy of an executable image** across all sessions running it. It loads the binary once and points other sessions at it; each session believes it has its own copy. Only when a session writes to that image does the server make a unique copy for it (copy-on-write).

Misleading effect: Task Manager reports the full memory amount for each user's session, so only the total figures reveal that the numbers do not add up.

**Committed vs working set**: committed memory is everything Windows granted a process (in RAM or paged). The **working set** is the part actually kept in physical RAM. When overall memory use is low Windows leaves whole working sets in RAM; once utilization passes ~80% it reclaims unused working-set pages to disk, which does not hurt performance since those pages were idle. Only when memory gets truly scarce does it page out actively-used working set, which is when users slow down.

These OS memory concepts are durable.

*Bron: Core Knowledge doc 'TS, Mem Usage, Shadow Key and (Flex) Profile Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Copy-on-Write Snapshots vs Clones](copy-on-write-snapshots-vs-clones.md)
- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [PowerFuse performance shields (reference)](powerfuse-performance-shields.md)
- [Why the page file matters in Terminal Server](terminal-server-page-file-copy-on-write.md)
- [Terminal Server / Citrix troubleshooting checklist (own notes)](terminal-server-troubleshooting-checklist.md)
