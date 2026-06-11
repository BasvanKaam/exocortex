---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, print-driver-isolation, printisolationhost, citrix, ica, spooler]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Print Driver Isolation modes and the Citrix Print Management Service

How it worked. Windows Server 2008 R2 introduced Print Driver Isolation with three modes:
- None (default): no isolation; a bad driver can still crash the machine.
- Shared: a group of print drivers runs together in a separate 'PrintIsolationHost' process, isolated from the Spooler and the Citrix Print Management service; a failure only affects drivers in that process.
- Isolated: each print driver gets its own PrintIsolationHost process. Maximum isolation but more local resource consumption.

Field guidance from Bas: use None and Shared in production, reserve Isolated for troubleshooting (temporarily, even in production). And question whether a driver that needs isolating belongs in production at all.

Citrix Print Management Service: introduced in 2005 alongside the EMF-based universal print driver. It talks directly to the Spooler (local or remote), talks to the local ICA client and compresses data over the ICA channel when the client printing pathway is used, and owns the ICA virtual channel for client printer mapping/creation - which is exactly what to check when troubleshooting auto-create printer failures.

*Bron: blogpost 'Citrix printing internals cheat sheet… Part one' (2015-10-27), basvankaam.com.*

## Verwante notities

- [Citrix client-printing pathway: spool on server, send back over ICA](citrix-client-printing-pathway.md)
- [Citrix Print Management Service](citrix-print-management-service.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [EMF vs XPS print file formats](emf-vs-xps-print-formats.md)
- [Most Citrix printing pain is still bad drivers and bad architecture](positie-citrix-printing-still-driver-and-design-problem.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Print driver versions and Print Driver Isolation](print-driver-history-and-modes.md)
- [Print driver isolation: None, Shared, Isolated](print-driver-isolation-modes.md)
- [Print spooling and the kernel-mode to user-mode driver history](windows-print-spooling-and-driver-history.md)
