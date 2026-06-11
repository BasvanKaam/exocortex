---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vmware, vmfs, storage, block-size, esxi]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VMFS3 vs VMFS5 block and sub-block sizing

How it worked then (vSphere 5.x era): VMFS5 (introduced with ESXi 5) builds on VMFS3 but isn't mandatory; upgrading ESXi hosts doesn't auto-upgrade datastores, and an upgraded VMFS3 datastore keeps its original block size.

- VMFS3 offered four block sizes (1/2/4/8 MB), max file size scaling from 256 GB to ~2 TB.
- VMFS5 offers a single 1 MB block size with up to 64 TB max file size.
- Sub-blocks store small files: VMFS3 uses 64 KB sub-blocks (4000 available), VMFS5 uses 8 KB (32000). A file only uses a sub-block if it is at or under the sub-block size; otherwise it consumes a full 1 MB file block. It never chains multiple sub-blocks.
- Compatibility: VMFS3 is forward/backward compatible up to v5; VMFS5 is not. All hosts sharing a VMFS5 datastore must run ESXi 5+.

*Bron: blogpost 'Block vs file level storage, VMware VMFS, NTFS and some of the protocols involved.' (2014-09-17), basvankaam.com.*

## Verwante notities

- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [Block vs file level storage, plainly](block-vs-file-storage.md)
- [Hyper-V vs VMware in 2013: cheaper and simpler vs granular](hyper-v-vs-vmware-cost-2013.md)
- [When someone quotes an IOPS number, ask which block size](iops-always-ask-block-size.md)
- [IOPS fundamentals: latency is king](iops-latency-fundamentals.md)
- [Server 2012 R2 opened up cheaper VDI storage options](server-2012-r2-cheaper-vdi-storage.md)
- [How share and NTFS permissions combine](share-vs-ntfs-permission-combination.md)
- [Why traditional SANs are complex for virtual workloads](traditional-san-complexity.md)
