---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, netscaler, tftp, pvs, load-balancing, high-availability]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler 10.1 TFTP load balancing for PVS boot HA

How it worked then. NetScaler 10.1 introduced simplified TFTP load balancing with intelligent monitoring. You bind a monitor to a TFTP virtual server, pick a load-balance method from a dropdown (Round Robin, Least Connection, Least Bandwidth, etc.), and point the virtual TFTP servers at the real TFTP servers. In DHCP you set option 66 to the NetScaler address and option 67 to the bootstrap filename. This gives high availability for the PVS boot/streaming path.

*Bron: blogpost 'Citrix Provisioning Services 7... A sneak preview' (2013-06-21), basvankaam.com.*

## Verwante notities

- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- [NetScaler monitors: why load balancing needs health checks](netscaler-monitors-health-checking.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
- [BDM disk removes the PXE/DHCP/TFTP dependency for PVS boot](pvs-bdm-disk-no-pxe-dhcp.md)
- [Killing VDI IOPS with PVS write cache in RAM](pvs-write-cache-in-ram.md)
