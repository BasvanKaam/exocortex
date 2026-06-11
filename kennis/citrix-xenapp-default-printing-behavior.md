---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, xenapp, printing, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix XenApp Default Printing Behavior

How XenApp printed with no policy rules configured (circa 2010):

- All printers configured on the client device are auto-created at the start of each session (equivalent to Auto-create client printers → Auto-create all client printers).
- Print jobs to printers locally attached to the client are routed as client print jobs, over the ICA channel through the client device.
- Jobs to network printers are routed directly from the server hosting the published application; if that fails, they are redirected through the client device (equivalent to disabling Direct connection to print servers).
- User-configured printer properties are retained, stored on the client device, or in the user profile if the client cannot store them (equivalent to Printer properties retention → Held in profile only if not saved on client).
- XenApp uses the Windows printer driver if present on the host server; otherwise it tries to install it from Windows; failing that it uses a Citrix Universal printer driver (equivalent to Automatic installation of in-box printer drivers plus Use universal printing only if requested driver is unavailable).

*Bron: Core Knowledge doc 'Citrix XenApp Printing Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Bas's checklist to speed up and clean up Citrix printing](bas-citrix-printing-optimization-checklist.md)
- [Citrix client vs network printing pathway](citrix-client-vs-network-printing-pathway.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [Citrix wfshell.exe, cltmgr.exe, and printer drivers (reference)](citrix-wfshell-cltmgr-printer-drivers.md)
- [Citrix XenApp Printing Pathways](citrix-xenapp-printing-pathways.md)
