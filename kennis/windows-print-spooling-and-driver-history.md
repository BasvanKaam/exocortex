---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, spooler, print-drivers, kernel-mode, user-mode, rpc, smb]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Print spooling and the kernel-mode to user-mode driver history

How it worked. Print spooling is the loop where the spooler service receives application print output, hands it to a print driver that renders it into a print job, gets it back, and sends it to the physical device. Spooling is local when the printer is locally attached (consumes local CPU/MEM) and remote when using a network-provisioned printer (consumes resources on the print server and generates RPC/SMB network traffic). In a Citrix session on a XenApp server, the printer is usually network-provisioned, so spooling is remote from the XenApp server's perspective - size both resources and network for this.

Driver history (why printing was a pain): Windows NT had only v2 kernel-mode drivers; a bad one could take down the whole machine. Windows 2000 brought v3 user-mode drivers (still widely used in 2015) - a bad one only loses the user-mode section, less catastrophic. Windows Server 2008 R2 began auto-blocking v2 kernel-mode driver installs. Windows Server 2012 added v4 drivers: user-mode, isolatable, XPS-only, built for metro-style apps, broader printer-type support.

*Bron: blogpost 'Citrix printing internals cheat sheet… Part one' (2015-10-27), basvankaam.com.*

## Verwante notities

- [Citrix client-printing pathway: spool on server, send back over ICA](citrix-client-printing-pathway.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Print driver versions and Print Driver Isolation](print-driver-history-and-modes.md)
- [Print Driver Isolation modes and the Citrix Print Management Service](print-driver-isolation-and-citrix-print-mgmt.md)
- [Print driver isolation: None, Shared, Isolated](print-driver-isolation-modes.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
- [Printing is the perennial pain admins shouldn't have to focus on](printing-is-a-perennial-euc-pain.md)
- [EMF vs XPS print file formats](windows-print-emf-vs-xps.md)
