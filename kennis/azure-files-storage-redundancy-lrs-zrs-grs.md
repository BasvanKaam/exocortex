---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure-files, fslogix, storage, redundancy, wvd]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Azure Files storage redundancy: LRS, ZRS, GRS

For WVD profile/user/departmental data on Azure Files (often with FSLogix Profile Containers and MSIX App Attach), redundancy is chosen at the storage account level:

- LRS (Locally redundant): every file stored 3x within a single Azure storage cluster. Protects against hardware failure like a bad disk. Single-datacenter.
- ZRS (Zone redundant): every file stored 3x across three distinct storage clusters in different Availability Zones. A write is not acknowledged until written to all three zones. Multi-datacenter.
- GRS (Geo-redundant, Azure Files Standard only): like LRS in the primary region (3 copies) plus asynchronous replication to a Microsoft-defined secondary region = 6 copies across two regions. Async replication means a non-zero RPO (minutes, not hours). On disaster, Microsoft fails over the secondary to primary (can also be manual).

Cost angle: more copies and more locations cost more; cross-zone egress between VMs became billable from Feb 2021, and cross-region (GEO) transfer is charged. Standard premium-tier Azure Files had a ~33% price drop announced around late 2020.

*Bron: blogpost 'How to Make Your 1,000+ User WVD Deployment Highly Available' (2020-12-07), basvankaam.com.*

## Verwante notities

- [Azure Availability Sets vs Availability Zones](azure-availability-sets-vs-zones.md)
- [Azure Ephemeral OS disks for stateless WVD workloads](azure-ephemeral-os-disks.md)
- [Azure Files: a cloud NAS, plus Azure File Sync for hybrid](azure-files-cloud-nas.md)
- [Azure high-availability building blocks](azure-high-availability-building-blocks.md)
- [Nerdio shines where Microsoft's WVD HA docs are missing](nerdio-fills-microsoft-wvd-ha-doc-gap.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [Synchronous vs Asynchronous Replication](synchronous-vs-asynchronous-replication.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
