---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [terminal-server, page-file, copy-on-write, memory, dll]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Why the page file matters in Terminal Server

A common misconception is that the page file is merely an extension of physical memory you can ignore by buying enough RAM. In Terminal Server environments that is wrong, because of **copy-on-write**.

Windows loads a single copy of a shared executable/DLL into memory, but every EXE and DLL is effectively written to as it runs (the in-memory version, not the file on disk). When a process writes to a shared section, Windows makes a private copy for it and also backs that section up to the page file. So a single shared DLL section can exist three ways: the original, the per-process writable copy, and the page-file backup.

With many users this multiplies. A fat client/server app (JD Edwards OneWorld, Cerner, Lotus Notes, Siebel, PeopleSoft, SAP) loads a core EXE plus many DLLs per session. For 30 users Windows initially loads one copy, then copy-on-write creates per-user copies and places matching copies in the page file, so a single executable can end up as roughly 59 copies across memory, multiplied across every EXE and DLL the app loads. These fat clients were never designed for Terminal Server.

Takeaway: the page file is heavily used regardless of how much physical memory you have. Durable concept about how shared-image copy-on-write drives page-file usage on multi-user servers.

*Bron: Core Knowledge doc 'TS, Mem Usage, Shadow Key and (Flex) Profile Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Copy-on-Write Snapshots vs Clones](copy-on-write-snapshots-vs-clones.md)
- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [How memory works in Terminal Server: shared executables](terminal-server-memory-shared-executables.md)
- [Why traditional Windows applications won't disappear](traditional-windows-applications-wont-disappear.md)
