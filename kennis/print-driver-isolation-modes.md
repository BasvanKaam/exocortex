---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, drivers, isolation, windows-server]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Print driver isolation: None, Shared, Isolated

How it worked then. Most print issues historically traced back to poorly written print drivers (Bas cites 80-90%): not optimized for multi-user, unsigned, causing hung spooler/Citrix Print Manager services, blue screens, auto-create failures, high CPU. Windows NT had only v2 kernel-mode drivers (a bad one took the whole system down); Windows 2000 brought v3 user-mode drivers (a failure stays in user mode); Server 2012 added v4 user-mode drivers, XPS-only, for Metro-style apps.

Server 2008 R2 introduced Print Driver Isolation with three modes. None (default): all drivers interact, one bad driver can still bring down the machine. Shared: a group of drivers runs in a separate 'PrintIsolationHost' process, isolated from the spooler and CTX Print Management Service. Isolated: one PrintIsolationHost process per driver, consuming more CPU/memory. Bas's guidance: use None/Shared in production and reserve Isolated for troubleshooting.

*Bron: blogpost 'The ultimate Citrix printing internals cheat sheet - version 2.0' (2017-08-28), basvankaam.com.*

## Verwante notities

- [Citrix Print Management Service](citrix-print-management-service.md)
- [Most Citrix printing pain is still bad drivers and bad architecture](positie-citrix-printing-still-driver-and-design-problem.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Print driver versions and Print Driver Isolation](print-driver-history-and-modes.md)
- [Print Driver Isolation modes and the Citrix Print Management Service](print-driver-isolation-and-citrix-print-mgmt.md)
- [Tools are fine, but understand the architecture before you troubleshoot](printing-troubleshooting-understand-architecture-first.md)
- [Tricerat Simplify: central driver management for direct IP printing (2018)](tricerat-simplify-driver-management.md)
- [Print spooling and the kernel-mode to user-mode driver history](windows-print-spooling-and-driver-history.md)
