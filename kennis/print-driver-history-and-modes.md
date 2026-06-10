---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, print-drivers, kernel-mode, print-driver-isolation]
layer: reference
bron: inside-citrix-fma
---

# Print driver versions and Print Driver Isolation

Historically, 80-90% of print issues traced back to poorly written print drivers: not optimized for multi-user, untested/unsigned, hanging services (spooler and Citrix Print Manager), blue screens, failed auto-creation, high CPU.

Driver history: Windows NT had only version 2 kernel-mode drivers (a bad one could take down the whole system). Windows 2000 introduced version 3 user-mode drivers (still widely used); a misbehaving v3 driver doesn't crash the kernel, though it can still render a server useless, just with less impact.

Windows Server 2008 R2 added a mechanism that automatically blocks installation of version 2 kernel-mode drivers, plus Print Driver Isolation with three modes:
- None (default): nothing changes; a bad driver can still bring down the machine.
- Shared: a group of drivers runs in a separate 'PrintIsolationHost' process, isolated from other drivers, the Print Spooler and the CTX Print Management Service, so a failure only affects that group.
- Isolated: isolation per individual driver, a separate PrintIsolationHost process each, consuming more local CPU/memory.

Version 4 mode drivers arrived with Windows Server 2012: user-based, isolatable, designed for Metro-style apps, XPS-exclusive, support more printer types, more stable, with enhanced sharing and easier install/maintenance.

FMA fact / Bas's advice: print driver isolation is often used for troubleshooting and testing; consider using None and Shared in production and Isolated only for troubleshooting (which can be in production, only temporarily). He also says to question why a driver needs isolation at all before putting it into production.

## Verwante notities

- [Bas's checklist to speed up and clean up Citrix printing](bas-citrix-printing-optimization-checklist.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [EMF vs XPS print file formats](emf-vs-xps-print-formats.md)
- [Microsoft print file formats: EMF vs XPS](microsoft-print-formats-emf-xps.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
- [Print-related troubleshooting tools (Print Detective, UPS Cert Tool, StressPrinters)](print-troubleshooting-tools.md)
