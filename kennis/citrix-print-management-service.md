---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, ctx-print-management, ica, virtual-channel]
layer: reference
bron: inside-citrix-fma
---

# Citrix Print Management Service

The Citrix Print Management Service was first introduced in 2005, around the same time as the EMF-based universal print driver. It directly communicates with the Print Spooler service and, when the client printing pathway is used, communicates with the locally installed ICA Client and compresses data before it's sent over the ICA channel. It is in charge of the ICA virtual channel for client printer mapping/creation within the CTX session, which is useful to know when troubleshooting auto-create printer failures.

## Verwante notities

- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Bas on why he likes Citrix printing](bas-likes-printing.md)
- [Citrix print troubleshooting tools](citrix-print-troubleshooting-tools.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
- [Citrix Universal Printer (logical print object)](citrix-universal-printer.md)
- [EMF vs XPS print file formats](emf-vs-xps-print-formats.md)
- [ICA virtual channel priorities (0-3) and how to change them](ica-virtual-channel-priorities.md)
- [ICA virtual channels: 32 total, 17 reserved by Citrix](ica-virtual-channels.md)
