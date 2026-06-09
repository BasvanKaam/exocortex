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
