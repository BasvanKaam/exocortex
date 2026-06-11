---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, printing, architecture, design, wan, endpoints]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Print architecture is decided by all elements combined, not one knob

A durable design principle from the printing deep-dive: there is no single setting that makes or breaks Citrix print performance. It's the combination of the endpoint types you use (Windows fat client vs Linux thin client), the physical placement of your machines (datacenter vs branch office), how you provision printers (locally attached vs print server), and which pathway results. Whether print traffic is compressed (over ICA) or not depends on whether both ends of a hop speak ICA. Design by reasoning about where spooling happens and which hops are uncompressed across the WAN.

*Bron: blogpost 'The ultimate Citrix printing internals cheat sheet! BIG Takeaway list included!' (2015-12-08), basvankaam.com.*

## Verwante notities

- [Bas's checklist to speed up and clean up Citrix printing](bas-citrix-printing-optimization-checklist.md)
- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Citrix client vs network printing pathway](citrix-client-vs-network-printing-pathway.md)
- [Citrix network vs client printing pathway](citrix-print-pathways-network-vs-client.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix XenApp Printing Pathways](citrix-xenapp-printing-pathways.md)
- [Direct IP printing: simple and cheap, but decentralized to manage](direct-ip-printing-tradeoffs.md)
- [Forcing the client pathway for network printers, and when not to](forcing-client-pathway-direct-connections-policy.md)
- [Most Citrix printing pain is still bad drivers and bad architecture](positie-citrix-printing-still-driver-and-design-problem.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
- [Printing is business critical, and underrated](printing-is-business-critical.md)
- [Tools are fine, but understand the architecture before you troubleshoot](printing-troubleshooting-understand-architecture-first.md)
- [EMF vs XPS print file formats](windows-print-emf-vs-xps.md)
- [Print spooling and the kernel-mode to user-mode driver history](windows-print-spooling-and-driver-history.md)
