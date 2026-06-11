---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, printing, ica, xenapp, print-pathway]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix network vs client printing pathway

How it worked then (XenApp era). The printing pathway is the route a print job takes to its destination, plus where it gets spooled. Routing affects network traffic; spooling affects local resource use on the XenApp or print server. Two pathways exist:

Network printing pathway: used by network-provisioned print devices. The job goes from the XenApp server hosting the session, uncompressed over the network, directly to the print server, where it is spooled and processed, then sent to the print device. Because the data is uncompressed, this hurts on a WAN (e.g. print server and device are remote from XenApp). Ideal for LANs, not WANs. Note: if XenApp and print server are in different domains with no trust, or no network path exists, XenApp automatically falls back to the client pathway.

Client printing pathway: the job is routed over the ICA protocol through the client device to the printer (locally attached, or a network printer via a print server) and spooled on the XenApp server. Advantage: ICA compresses the data, so even across a WAN the transfer is compressed.

*Bron: blogpost 'Citrix Printing Pathway... an overview' (2013-01-10), basvankaam.com.*

## Verwante notities

- [Citrix client-printing pathway: spool on server, send back over ICA](citrix-client-printing-pathway.md)
- [Citrix client vs network printing pathway](citrix-client-vs-network-printing-pathway.md)
- [Citrix network-printing pathway: print-server traffic is uncompressed](citrix-network-printing-pathway.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Forcing the client pathway for network printers, and when not to](forcing-client-pathway-direct-connections-policy.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Tools are fine, but understand the architecture before you troubleshoot](printing-troubleshooting-understand-architecture-first.md)
