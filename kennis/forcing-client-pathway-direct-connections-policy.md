---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, printing, print-policy, ica, session-printer]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Forcing the client pathway for network printers, and when not to

How it worked then. You can make XenApp route network-provisioned print jobs through the client device (gaining ICA compression) by disabling the Citrix policy 'Direct connections to print servers'. Citrix recommends this when the print server and device sit remote from XenApp but near the clients.

But topology matters. If XenApp and the print server are on site one and the clients/printer are on site two, disabling the policy causes wasteful round trips: data goes XenApp -> client (site one to two, compressed via ICA), then client -> print server (site two back to one, uncompressed), then print server -> print device (site one to two, uncompressed). That is two extra, uncompressed transfers versus just leaving the policy enabled. So only force the client pathway when the physical layout justifies it.

The 'session printer' Citrix policy lets you auto-create specific network printers that still use the network pathway even when the rest is forced onto the client pathway, so you can mix both (e.g. one fast-LAN network printer alongside client-pathway printing).

*Bron: blogpost 'Citrix Printing Pathway... an overview' (2013-01-10), basvankaam.com.*

## Verwante notities

- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Citrix client-printing pathway: spool on server, send back over ICA](citrix-client-printing-pathway.md)
- [Citrix client vs network printing pathway](citrix-client-vs-network-printing-pathway.md)
- [Citrix network-printing pathway: print-server traffic is uncompressed](citrix-network-printing-pathway.md)
- [Citrix network vs client printing pathway](citrix-print-pathways-network-vs-client.md)
- [Citrix proximity printing](citrix-proximity-printing.md)
- [Citrix XenApp Printing Pathways](citrix-xenapp-printing-pathways.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
