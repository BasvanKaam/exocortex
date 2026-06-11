---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, xenapp, printing, ica, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix XenApp Printing Pathways

XenApp routes jobs to a network printing device by one of two paths:

**Network printing pathway:** the job goes from the farm server hosting the user's session over a network connection to the network print server, which spools it remotely and sends it to the printer. The application tells the remote spooler to create the job and spool file, the Windows Print Provider sends the spool file to the print server, the server processes it and sends it to the printer.

**Client printing pathway:** the job is routed over ICA through the client device to the printer (directly attached or via a print server) and spooled on the Citrix online plug-in. A virtual printer in the session redirects to the client's printer object. Because all processing is on the XenApp server, jobs are spooled locally on that server first.

- *Locally attached client printers:* the host server's local spooler renders the job with the printer driver, delivers the rendered data over ICA to the client, and the client relays it to the attached printer.
- *Client printers on the network:* same as above, but instead of going to a local printer the client sends the job over the network to the print server, which sends it to the network printer. Useful when the print server is in a different domain from the farm servers but the client devices can reach the print server's domain — the application servers send jobs over ICA to reach the printer through the client device.

*Bron: Core Knowledge doc 'Citrix XenApp Printing Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix client-printing pathway: spool on server, send back over ICA](citrix-client-printing-pathway.md)
- [Citrix network-printing pathway: print-server traffic is uncompressed](citrix-network-printing-pathway.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix wfshell.exe, cltmgr.exe, and printer drivers (reference)](citrix-wfshell-cltmgr-printer-drivers.md)
- [Citrix XenApp Default Printing Behavior](citrix-xenapp-default-printing-behavior.md)
- [Forcing the client pathway for network printers, and when not to](forcing-client-pathway-direct-connections-policy.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
