---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure-files, fslogix, lrs, zrs, grs, storage, redundancy, wvd, explainer]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Azure Files storage redundancy: LRS, ZRS, GRS

Data-side HA for WVD, where profile/user/departmental data sits on Azure Files (often Premium tier, paired with FSLogix Profile Containers and MSIX App Attach). Azure Files is the direct replacement for a traditional file server without managing an actual file server VM. Redundancy is chosen at the storage account level:

- **LRS (Locally redundant):** every file stored 3 times within a single Azure storage cluster. Protects against hardware failure like a bad disk. Single-datacenter config.
- **ZRS (Zone redundant):** every file stored 3 times across 3 distinct storage clusters in 3 different Availability Zones. A write is not acknowledged until written to all three zones (synchronous). Multi-datacenter config.
- **GRS (Geo-redundant, Azure Files Standard only):** like LRS in the primary region (3 copies) plus asynchronous replication to a Microsoft-defined secondary region = 6 copies across two regions. On disaster, Microsoft fails over the secondary to primary (can also be done manually).

**Trade-off Bas flags:** GRS async replication means a non-zero RPO (Recovery Point Objective) - minutes, not hours, but worth thinking about. More copies and more locations cost more.

Cost angle: cross-zone egress between VMs became billable from Feb 2021, and cross-region (GEO) transfer is charged. Standard premium-tier Azure Files had a ~33% price drop announced around late 2020.

*Bron: blogpost 'How to Make Your 1,000+ User WVD Deployment Highly Available' (2020-12-07), basvankaam.com / Nerdio-content 'Making your 1000+ user WVD deployment highly available!' (Blogs).*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [Azure Availability Sets vs Availability Zones](azure-availability-sets-vs-zones.md)
- [Azure Files: a cloud NAS, plus Azure File Sync for hybrid](azure-files-cloud-nas.md)
- [Azure Files tiers and pricing model (reference)](azure-files-tiers-reference.md)
