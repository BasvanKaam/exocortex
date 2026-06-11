---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, printing, ica, client-printing-pathway, xenapp, thin-client]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix client-printing pathway: spool on server, send back over ICA

How it worked then (XenApp era): in the client-printing pathway there is no print server by default. The user has a session on the XenApp server; on print, the output is spooled/rendered into a print job on the Citrix server, then sent back over ICA to the client device, which forwards it to the physical printer. Because both client and server run the Citrix Receiver / ICA stack, this traffic travels over ICA channels and can therefore be compressed and limited, which matters when client and server are physically separated. Catch: most thin clients are Linux-based and cannot locally process these print jobs, so the client-printing pathway only works with Windows (fat) clients. When a locally attached printer is configured on a Windows fat client, the client-printing pathway is enforced.

*Bron: blogpost 'The ultimate Citrix printing internals cheat sheet! BIG Takeaway list included!' (2015-12-08), basvankaam.com.*

## Verwante notities

- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Citrix client vs network printing pathway](citrix-client-vs-network-printing-pathway.md)
- [Citrix network-printing pathway: print-server traffic is uncompressed](citrix-network-printing-pathway.md)
- [Citrix Print Management Service](citrix-print-management-service.md)
- [Citrix network vs client printing pathway](citrix-print-pathways-network-vs-client.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix XenApp Printing Pathways](citrix-xenapp-printing-pathways.md)
- [Forcing the client pathway for network printers, and when not to](forcing-client-pathway-direct-connections-policy.md)
- [Print Driver Isolation modes and the Citrix Print Management Service](print-driver-isolation-and-citrix-print-mgmt.md)
- [Print spooling and the kernel-mode to user-mode driver history](windows-print-spooling-and-driver-history.md)
