---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, printing, ica, xenapp, pathways]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix client vs network printing pathway

How it worked then (Citrix native printing). A printing pathway defines how print traffic is routed and where jobs get spooled. Client pathway: the print job is spooled on the Citrix/XenApp server, then sent back to the client device over ICA, where it can be compressed/managed by the Citrix Print Management Service. Works only with Windows (fat) client devices; a locally attached client printer forces the client pathway. Network pathway: with network-provisioned (print server) printers, Citrix tries this first; the job is sent to the print server's spooler. Only the XenApp server speaks ICA here, so traffic between XenApp server and print server (and from print server to device) is uncompressed.

You can force the client pathway by disabling the 'Direct connection to print server' policy. This helps when the XenApp server is in the datacenter and the print server sits near users (compressing the WAN hop over ICA), but it makes things worse when the print server is back in the datacenter, because the job traverses the WAN uncompressed twice. If the XenApp server and print server cannot communicate, the client pathway is forced; with thin clients that can mean no printing at all.

*Bron: blogpost 'The ultimate Citrix printing internals cheat sheet - version 2.0' (2017-08-28), basvankaam.com.*

## Verwante notities

- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Citrix client-printing pathway: spool on server, send back over ICA](citrix-client-printing-pathway.md)
- [Citrix network-printing pathway: print-server traffic is uncompressed](citrix-network-printing-pathway.md)
- [Citrix Print Management Service](citrix-print-management-service.md)
- [Citrix network vs client printing pathway](citrix-print-pathways-network-vs-client.md)
- [Forcing the client pathway for network printers, and when not to](forcing-client-pathway-direct-connections-policy.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Tools are fine, but understand the architecture before you troubleshoot](printing-troubleshooting-understand-architecture-first.md)
