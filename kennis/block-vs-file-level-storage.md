---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [storage, san, nas, iscsi, nfs, fundamentals]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Block vs file level storage: the durable trade-off

Block storage (typically SAN, accessed via iSCSI or Fibre Channel): raw volumes (LUNs) are presented to a host and seen as individual hard drives, then formatted with a file system (NTFS, VMFS). Very flexible, high performance, but expensive and complex to manage (LUN management per host, SAN switches, HBAs, dedicated storage teams).

File storage (typically NAS, accessed via SMB/CIFS on Windows or NFS on Linux/VMware): a repository of disks exposed directly over the network via shares. Easier and faster to set up, cheaper mass storage per GB, but performance can be a concern and access/permissions often have to be managed on the NAS device's own OS.

Durable summary: block = flexible + fast + complex + costly; file = simple + cheap + potentially slower. Choice depends on workload needs and budget. The underlying conceptual split outlives any specific product.

*Bron: blogpost 'Block vs file level storage, VMware VMFS, NTFS and some of the protocols involved.' (2014-09-17), basvankaam.com.*

## Verwante notities

- [Block vs file level storage, plainly](block-vs-file-storage.md)
- [When someone quotes an IOPS number, ask which block size](iops-always-ask-block-size.md)
- [IOPS fundamentals: latency is king](iops-latency-fundamentals.md)
- [Older SAN/NAS isn't dead; flash caching keeps it alive](legacy-storage-extended-by-flash.md)
- [Server 2012 R2 opened up cheaper VDI storage options](server-2012-r2-cheaper-vdi-storage.md)
- [Why traditional SANs are complex for virtual workloads](traditional-san-complexity.md)
- [VMFS3 vs VMFS5 block and sub-block sizing](vmfs3-vmfs5-block-sizes.md)
