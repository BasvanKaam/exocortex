---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, printing, network-printing-pathway, print-server, xenapp, wan, branch-office]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix network-printing pathway: print-server traffic is uncompressed

How it worked then: with network-provisioned printers (a print server), Citrix tries to use the network-printing pathway by default. The XenApp server sends output to the print server's spooler, where it is spooled/rendered, then sent to the physical printer. The key gotcha: only the XenApp server runs the ICA stack; the print server does not understand ICA channels, so all traffic between the XenApp server and the print server is unmanaged and uncompressed. The job from print server to physical device is also uncompressed. This is fine when XenApp server and print server sit close together, but becomes a WAN problem when the XenApp server is in the datacenter and the print server is near users in a branch office (or vice versa).

*Bron: blogpost 'The ultimate Citrix printing internals cheat sheet! BIG Takeaway list included!' (2015-12-08), basvankaam.com.*

## Verwante notities

- [Citrix client-printing pathway: spool on server, send back over ICA](citrix-client-printing-pathway.md)
- [Citrix client vs network printing pathway](citrix-client-vs-network-printing-pathway.md)
- [Citrix network vs client printing pathway](citrix-print-pathways-network-vs-client.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
- [Citrix XenApp Printing Pathways](citrix-xenapp-printing-pathways.md)
- [Direct IP printing: simple and cheap, but decentralized to manage](direct-ip-printing-tradeoffs.md)
- [Forcing the client pathway for network printers, and when not to](forcing-client-pathway-direct-connections-policy.md)
