---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, print-drivers, best-practice, troubleshooting]
layer: rich
bron: inside-citrix-fma
---

# Bas's print driver best practices

Bas's view: most print issues trace back to badly written drivers not tested or optimised for multi-user environments — causing spooler crashes, CTX print manager service crashes, blue screens, auto-print-creation failures and high CPU. His rules:

- Do NOT use kernel-mode (version 2) print drivers; use user-mode (version 3 and 4) drivers exclusively. Version 4 drivers are designed for Metro/XPS apps with enhanced sharing and easier management.
- Use signed drivers only and always thoroughly test your print setup, no matter how convinced you are it will work.
- Limit the number of print drivers installed — less is more.
- Avoid upgrading print drivers; uninstall the old one and install the new.
- Always match the print server OS to the XenApp server OS.
- Consider Print Driver Isolation (introduced in Windows Server 2008 R2) — but only where it makes sense.
- Consider 'printer driver mapping compatibility' when client and server driver names differ but offer the same function; it can also build a whitelist of drivers allowed to auto-install.

The 'simpler' the print driver, the less traffic it generates — use vendor drivers only when specific functionality is needed.

## Bron-citaten (NL, verbatim)

> Do NOT make use of kernel mode (version 2) print drivers.
>
> Limit the number of print drivers installed: less is more!

## Verwante notities

- [Bas's checklist to speed up and clean up Citrix printing](bas-citrix-printing-optimization-checklist.md)
- [Citrix print troubleshooting tools](citrix-print-troubleshooting-tools.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [Citrix wfshell.exe, cltmgr.exe, and printer drivers (reference)](citrix-wfshell-cltmgr-printer-drivers.md)
- [EMF vs XPS print file formats](emf-vs-xps-print-formats.md)
- [Print driver versions and Print Driver Isolation](print-driver-history-and-modes.md)
- [Print Driver Isolation modes and the Citrix Print Management Service](print-driver-isolation-and-citrix-print-mgmt.md)
- [Print driver isolation: None, Shared, Isolated](print-driver-isolation-modes.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
- [Print-related troubleshooting tools (Print Detective, UPS Cert Tool, StressPrinters)](print-troubleshooting-tools.md)
- [Tools are fine, but understand the architecture before you troubleshoot](printing-troubleshooting-understand-architecture-first.md)
