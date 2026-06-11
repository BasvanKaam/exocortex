---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, client-pathway, network-pathway, ica, thin-clients]
layer: reference
bron: inside-citrix-fma
---

# Citrix printing pathways: client vs network

A printing pathway defines how print traffic is routed, and where it's processed and spooled. The physical setup and Citrix print policies let you partly influence it.

Server local printers: a physical printer attached directly to a XenApp server; spooling is local on the XenApp server (rare but useful).

Client printing pathway: typically used when a printer is locally attached to the client device, with no print server involved. Print traffic generated on the XenApp server is redirected back to the client, then to the physical printer. Spooling happens locally on the XenApp server; the spooled job is sent back to the client over the ICA protocol/virtual channels, so it can be compressed/limited (this is where the Citrix Print Management Service comes in). Both the client device and the XenApp server need Receiver/ICA. Note: most thin clients run Linux and can't process print jobs locally, so the client printing pathway only works with Windows (fat) clients; consider the Universal Print Server otherwise. With a locally attached printer on a Windows fat client, the client printing pathway is enforced.

Network printing pathway: with network-provisioned printers (print server), Citrix tries to use this pathway by default. Output is sent to the print server's spooler, spooled/rendered, then sent to the device. Only the XenApp server has Receiver/ICA; the print server can't use ICA, so traffic between XenApp server and print server is unmanageable/uncompressed, and the print server-to-device traffic is also uncompressed. Placement matters: a print server far from the XenApp server (e.g. in a branch office while XenApp is in the datacenter) can cause problems. If the XenApp server and print server can't communicate or aren't in the same domain, the client printing pathway is used (forced) instead, and with thin clients printing may then fail entirely.

FMA fact: it's not one thing but everything combined that makes or breaks a print architecture: endpoint types, configured policies, and the physical placement of machines and printers.

## Verwante notities

- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Bas on why he likes Citrix printing](bas-likes-printing.md)
- [Citrix client-printing pathway: spool on server, send back over ICA](citrix-client-printing-pathway.md)
- [Citrix Print Management Service](citrix-print-management-service.md)
- [Citrix network vs client printing pathway](citrix-print-pathways-network-vs-client.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways.md)
- [Citrix proximity printing](citrix-proximity-printing.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
- [Citrix XenApp Printing Pathways](citrix-xenapp-printing-pathways.md)
- [EMF vs XPS print file formats](emf-vs-xps-print-formats.md)
- [ICA virtual channel priorities (0-3) and how to change them](ica-virtual-channel-priorities.md)
- [Microsoft print file formats: EMF vs XPS](microsoft-print-formats-emf-xps.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
- [Universal Print Driver, Universal Printer and Universal Print Server](universal-print-driver-server-printer.md)
