---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, client-pathway, network-pathway, ica, thin-client]
layer: reference
bron: inside-citrix-fma
---

# Citrix printing pathways: client vs network

A printing pathway defines how print traffic is routed and where it is processed/spooled/rendered. There are two Citrix pathways (plus 'Server local printers' for a device directly attached to a XenApp server):

- Client printing pathway: print output is spooled/rendered on the XenApp server, then sent to the client over ICA — so it can be managed/compressed. Used automatically when a fat client has a local printer, and when TCP/IP direct printers are added (treated as locally attached). Thin clients (Linux-based) lack local printing and cannot use this pathway.
- Network printing pathway: output goes from the XenApp server to a print server where it is spooled/rendered remotely, then to the physical device. Traffic between XenApp and print server is uncompressed/unmanaged (non-ICA) unless the Universal Print Server is used. Used automatically for network-provisioned printers (and required for thin clients via session printers).

If the print server and XenApp server cannot communicate (e.g. different domains), Citrix falls back to the client printing pathway. Disabling the 'Direct connection to print servers' policy forces the client pathway even with network printers. This applies to both XenApp and XenDesktop and is neither IMA- nor FMA-specific.

## Verwante notities

- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Citrix Print Management Service](citrix-print-management-service.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix proximity printing](citrix-proximity-printing.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
