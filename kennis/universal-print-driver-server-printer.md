---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, upd, universal-print-server, universal-printer, proximity-printing]
layer: reference
bron: inside-citrix-fma
---

# Universal Print Driver, Universal Printer and Universal Print Server

The Universal Print Driver (UPD) is installed as part of the VDA but disabled by default. There are EMF and XPS UPD variants; EMF is used by default (changeable via policy). Both the Universal Print Server and Universal Printer use the UPD by default.

- Universal Printer: a logical/generic object created at the start of a session, mapped to the client's default printer (changeable). It skips print mapping/enumeration, speeding logon, but works only for Windows devices. Useful with the 'Wait for printer to be created' policy or when needing multiple local/network printers.
- Universal Print Server (UPS): a UPClient (on XenApp) plus UPServer (on print server) component, optimised for network printers with extra compression and QoS. Supports EMF and XPS drivers, works for thin clients and tablets via session printers, does not support client-side rendering (output goes straight to the print server), handles up to 50 print jobs per minute, and enables proximity printing (filtering sessions by IP/subnet so users hit the closest printer). Network printers leverage the UPS automatically via auto-discovery. Recommended for remote-office scenarios; test for adequate compression.

## Verwante notities

- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix proximity printing](citrix-proximity-printing.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
- [Citrix Universal Printer (logical print object)](citrix-universal-printer.md)
- [Universal Print Server load balancing and HA (7.9)](ups-load-balancing-ha.md)
