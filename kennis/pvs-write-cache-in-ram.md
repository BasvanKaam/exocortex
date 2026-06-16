---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [pvs, write-cache, iops, citrix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Killing VDI IOPS with PVS write cache in RAM

How it worked then: Citrix Provisioning Services (PVS) streams a read-only base image over the network to many VMs at once. Writes go to a write cache (like a differencing disk), which can be stateless or persistent and placed in several locations: device hard drive, device RAM, device RAM with overflow to disk (Win7 / Server 2012+), server disk stateless, or server disk persisted.

To eliminate IOPS you want cache in device RAM (the RAM of the hypervisor host where the VM runs, so size accordingly), ideally with overflow-to-disk to avoid blue screens on memory exhaustion. RAM cache only suits pooled desktops since RAM isn't permanent. PVS also caches reads in the PVS server's RAM, so streaming the same blocks to VM 2, 3, 4 costs no extra storage IOPS.

Trade-off: if the host crashes, writes in RAM are lost and users may lose work; same if the PVS server dies with cache on its local disk.

*Bron: blogpost 'VDI, storage and the IOPS that come with it. Part 1 & 2.' (2013-11-12), basvankaam.com.*

## Verwante notities

- [NetScaler 10.1 TFTP load balancing for PVS boot HA](netscaler-tftp-load-balancing-pvs.md)
- [The five VDI workload phases and boot/logon storms](vdi-workload-phases-storms.md)
