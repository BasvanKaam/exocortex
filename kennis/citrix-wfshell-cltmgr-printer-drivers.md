---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, wfshell, cltmgr, printing, drivers, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix wfshell.exe, cltmgr.exe, and printer drivers (reference)

When Citrix is in the picture, UserInit also runs **CmStart.exe**, which does two things:

1. Starts the Citrix seamless windows engine shell, **wfshell.exe**.
2. Launches the Citrix Client Manager, **cltmgr.exe**, which keeps the ICA client up to date (it reads the client version from version.dat over the VDCM.dll ClientManagement virtual channel).

One of wfshell's jobs is autocreating client printers. Using third-party printer drivers (HP, Canon, Lexmark) instead of the in-box Windows drivers could cause wfshell.exe crashes, high CPU spikes, slow logons, and unmapped printers.

Advice captured from the field: avoid third-party printer drivers, use mappings from the printer matrix, and at minimum avoid PCL6 drivers (an advice credited to Stefan). If the client update feature is unused, disable the client update database on every Citrix server (cudutil.exe) to prevent cltmgr-related crashes and slow logons.

Dated reference; product-specific to the MetaFrame/XenApp era.

*Bron: Core Knowledge doc 'Citrix TS Logon Proces Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix Receiver: purpose and naming history](citrix-receiver-history-and-purpose.md)
- [Citrix / Terminal Services logon sequence (reference)](citrix-ts-logon-sequence.md)
- [Citrix XenApp Default Printing Behavior](citrix-xenapp-default-printing-behavior.md)
- [Citrix XenApp Printing Pathways](citrix-xenapp-printing-pathways.md)
- [Most Citrix printing pain is still bad drivers and bad architecture](positie-citrix-printing-still-driver-and-design-problem.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Terminal Server AppSetup key and UsrLogon.cmd (reference)](ts-appsetup-key-and-usrlogon.md)
