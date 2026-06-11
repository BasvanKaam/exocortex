---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vdi, storage, windows-server-2012-r2, storage-spaces, iops]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Server 2012 R2 opened up cheaper VDI storage options

How it worked then (2013): Windows Server 2012 R2 RDS added support for simpler, cheaper storage as an alternative to expensive SAN, which Bas saw as a major lever for VDI adoption.

- Directly Attached Storage (DAS) and plain SMB 3.0 file shares became viable backends.
- Storage Spaces: storage virtualization built from JBOD (just a bunch of disks), configured from within the OS via storage pools.
- Storage tiering (tech Microsoft acquired from StorSimple): frequently used data on SSD, cold data on cheap HDD, SSDs and HDDs coexisting in one pool with the system handling placement.
- Data de-duplication extended to live running VMs (VHD/VHDX in use).
- Storage QoS: throttle disruptive VMs to a max IO threshold, or alert on IO-starved VMs, configurable while running.

Bas's framing: storage cost and complexity is one of the main reasons VDI never took off as hoped, so cheaper storage matters more than the headline feature.

*Bron: blogpost 'A closer look at the Cloud, based on Server 2012 R2' (2013-10-26), basvankaam.com.*

## Verwante notities

- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [Hyper-V vs VMware in 2013: cheaper and simpler vs granular](hyper-v-vs-vmware-cost-2013.md)
- [IOPS fundamentals: latency is king](iops-latency-fundamentals.md)
- [Older SAN/NAS isn't dead; flash caching keeps it alive](legacy-storage-extended-by-flash.md)
- [SDN via Hyper-V network virtualization (how it worked in 2012 R2)](sdn-network-virtualization-2012r2.md)
- [Server 2012 R2 data dedup and the VDI separation rule](server-2012-r2-dedup-for-vdi.md)
- [Why traditional SANs are complex for virtual workloads](traditional-san-complexity.md)
- [VMFS3 vs VMFS5 block and sub-block sizing](vmfs3-vmfs5-block-sizes.md)
