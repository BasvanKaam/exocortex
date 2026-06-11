---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, spooling, print-server, network-traffic]
layer: reference
bron: inside-citrix-fma
---

# Print spooling: local vs remote

Print spooling is the process where application print output is received by the spooler service (which interprets EMF files and can insert page layout/job control info in the GDI/EMF case), hands it to a print driver that renders it into a print job, then sends it back to the spooler and on to the physical print device.

With local spooling, local CPU and memory are consumed (e.g. a PC with a locally attached printer). With a network-provisioned printer via a print server, spooling happens remotely on the print server, consuming its resources and generating network traffic between the client (which could be a XenApp server) and the print server per job. Both must be considered when sizing a print architecture. Local spooling uses no network resources.

Even in non-Citrix environments, high-latency WANs give poor user experience if jobs spool remotely across the WAN. However, remote spooling is preferable when local resources are needed for other tasks, since processing is offloaded to the print server.

## Verwante notities

- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix proximity printing](citrix-proximity-printing.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
- [EMF vs XPS print file formats](emf-vs-xps-print-formats.md)
- [Microsoft print file formats: EMF vs XPS](microsoft-print-formats-emf-xps.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Print driver versions and Print Driver Isolation](print-driver-history-and-modes.md)
- [Print spooling and the kernel-mode to user-mode driver history](windows-print-spooling-and-driver-history.md)
