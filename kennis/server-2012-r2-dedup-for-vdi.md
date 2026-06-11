---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [data-deduplication, windows-server-2012-r2, vdi, storage, hyper-v]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Server 2012 R2 data dedup and the VDI separation rule

How it worked then: data deduplication eliminates duplicate chunks to improve storage utilization, working best on static data (savings up to ~90% depending on data type). In Server 2012 default policy deduplicated files not modified for 5 days; customers pushed it harder (3 days, all data, even running VHD libraries), which didn't work, so Microsoft re-designed it in R2 to handle open and in-use files including VHDs.

Key constraint: to support dedup of open/in-use VHDs for VDI, Microsoft required the storage node and the VDI compute node (the Hyper-V hosts) to be physically separated / remotely connected, because of dedup's performance impact. Microsoft's wording: they 'do not support deduplication of arbitrary in use VHDs', but since dedup is part of the storage stack there's no explicit block, so it can technically be enabled on other workloads. Practical payoff: huge space savings, or reinvest the saved capacity in SSDs for 50%+ read/write speed gains.

*Bron: blogpost 'VIAB and Windows Server 2012 R2's Data Deduplication' (2013-11-20), basvankaam.com.*

## Verwante notities

- [IOPS fundamentals: latency is king](iops-latency-fundamentals.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [SDN via Hyper-V network virtualization (how it worked in 2012 R2)](sdn-network-virtualization-2012r2.md)
- [Server 2012 R2 opened up cheaper VDI storage options](server-2012-r2-cheaper-vdi-storage.md)
- [Why traditional SANs are complex for virtual workloads](traditional-san-complexity.md)
- [VDI-in-a-Box: the simplified all-in-one VDI appliance](vdi-in-a-box-architecture.md)
- [VIAB vs XenDesktop: simplicity vs flexibility tradeoffs (2013)](viab-vs-xendesktop-tradeoffs.md)
