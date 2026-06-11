---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [iops, storage, performance, benchmarking]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# When someone quotes an IOPS number, ask which block size

Cluster/block size (allocation unit size) is the smallest amount of disk space used to hold a file; files round up to the next multiple. It also directly affects IOPS measurement.

Bas's durable rule: "when someone states that their storage solution can do a million IOPS, ask them which block size was used." A headline IOPS figure is meaningless without the block size (and the read/write mix, queue depth, etc.) behind it. A timeless guard against vendor benchmark inflation.

*Bron: blogpost 'Block vs file level storage, VMware VMFS, NTFS and some of the protocols involved.' (2014-09-17), basvankaam.com.*

## Verwante notities

- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [Block vs file level storage, plainly](block-vs-file-storage.md)
- [The five VDI workload phases and boot/logon storms](vdi-workload-phases-storms.md)
- [VMFS3 vs VMFS5 block and sub-block sizing](vmfs3-vmfs5-block-sizes.md)
