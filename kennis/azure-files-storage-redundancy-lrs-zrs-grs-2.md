---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [azure-files, fslogix, lrs, zrs, grs, storage, redundancy, explainer]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Azure Files storage redundancy for WVD profiles: LRS vs ZRS vs GRS

Bas's explainer on data-side HA for WVD, where profile/departmental data sits on Azure Files (often Premium, paired with FSLogix Profile Containers and MSIX AppAttach). Azure Files is the direct replacement for a traditional file server without managing an actual file server VM.

- **LRS (Locally redundant):** every file stored 3 times within one Azure storage cluster. Protects against hardware failure (bad disk). Single-datacenter config.
- **ZRS (Zone redundant):** every file stored 3 times across 3 distinct storage clusters in 3 different Availability Zones. Multi-datacenter config. A write is not acknowledged until written to all three zones (synchronous).
- **GRS (Geo redundant):** like LRS in the primary region (3 copies), then asynchronously replicated to a Microsoft-defined secondary region = 6 copies across 2 regions. Microsoft fails over on disaster (can also be done manually). GRS is Azure Files Standard only.

**Trade-off Bas flags:** GRS async replication impacts RPO (Recovery Point Objective) - minutes, not hours, but worth thinking about. More copies / more locations = higher cost.

Links to: WVD high availability architecture, FSLogix, MSIX AppAttach.

*Bron: Nerdio-content 'Making your 1000+ user WVD deployment highly available!' (Blogs).*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [Azure Availability Sets vs Availability Zones](azure-availability-sets-vs-zones.md)
- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [Azure Files tiers and pricing model (reference)](azure-files-tiers-reference.md)
- [FSLogix benefits for WVD (and on-premises)](fslogix-benefits-for-wvd-and-on-premises.md)
- [WVD high availability: what you actually own vs what Microsoft owns](wvd-high-availability-architecture.md)
