---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [storage, block, file, san, nas, iops]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Block vs file level storage, plainly

Bas's plain-language distinction:

- Block level: raw storage volumes (blocks), e.g. a SAN's disks split into raw volumes accessed over Fibre Channel or iSCSI. Each block behaves like an individual hard drive (format NTFS/NFS/VMFS). Most flexible and high-performing, but harder to manage and more expensive.
- File level: usually a NAS, one big pile of files and folders reached via SMB, CIFS or NFS. Cheap and easy, but not built for high load. A NAS has its own non-standard OS handling files, so watch user access control and AD permissions.

Rule of thumb: heavy read/write load (like hundreds of VDI VMs) needs block storage; file storage won't cut it.

*Bron: blogpost 'VDI, storage and the IOPS that come with it. Part 1 & 2.' (2013-11-12), basvankaam.com.*

## Verwante notities

- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [When someone quotes an IOPS number, ask which block size](iops-always-ask-block-size.md)
- [IOPS fundamentals: latency is king](iops-latency-fundamentals.md)
- [Why traditional SANs are complex for virtual workloads](traditional-san-complexity.md)
- [The five VDI workload phases and boot/logon storms](vdi-workload-phases-storms.md)
- [VMFS3 vs VMFS5 block and sub-block sizing](vmfs3-vmfs5-block-sizes.md)
