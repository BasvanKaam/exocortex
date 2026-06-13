---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, wvd, high-availability, azure, disaster-recovery, fslogix, azure-files]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# AVD High Availability: Availability Sets vs Zones and Redundant Storage

With AVD/WVD the broker, gateway, load balancing, database and web portal are Microsoft-managed and made highly available by Microsoft. What you own is the **VMs and the data** (profiles, personal and departmental data). HA is your job only for those two layers.

## Availability Sets (single-datacenter redundancy)
- Spreads VMs across **fault domains** (shared power/network switch, like an on-prem rack) and **update domains** (hardware that can be patched/rebooted together).
- Default for ARM/WVD deployments: up to **3 fault domains**, **5 (non-configurable) update domains** (a 6th VM wraps back to the first update domain).
- Think of an Availability Set as a **local-datacenter** redundancy option. All data still sits in one datacenter.

## Availability Zones (datacenter-level failure protection)
- Unique physical locations within an Azure region, each with independent power, cooling, networking. Minimum 3 zones in enabled regions.
- Zones are themselves combinations of fault and update domains. 3+ VMs across 3 zones = effectively 3 fault and 3 update domains, one per zone.
- Zones are usually **20-50 miles apart**, connected by very fast links. Use Zones for **datacenter-level** failures.
- A **99.99% VM uptime SLA** applies with two or more VMs across two or more Availability Zones in a region.

## Data redundancy (Azure Files / storage accounts)
- **LRS** (Locally redundant): file stored 3x within one storage cluster; protects against disk/hardware faults. Single-datacenter.
- **ZRS** (Zone redundant): file stored 3x across 3 distinct clusters in different Availability Zones. A write is not acknowledged until written to all three zones. Multi-datacenter.
- **GRS** (Geo redundant, Azure Files Standard only): like LRS in the primary region plus asynchronous replication to a Microsoft-defined secondary region = 6 copies across 2 regions. Async replication impacts **RPO** (minutes, not hours).

## Costs
- Availability Sets and Zones are **free** and do not duplicate machines; the one machine is spread across domains/zones.
- You pay for storing data multiple times (redundant storage), and for **egress between VMs across Availability Zones** (billed since Feb 2021) and cross-region traffic for GEO redundancy.

This is the low-hanging fruit of an AVD DR plan, not the whole plan.

*Bron: Nerdio-content 'Making your WVD deployment highly available' (Blogs).*

## Verwante notities

- [Azure Availability Sets vs Availability Zones](azure-availability-sets-vs-zones.md)
- [Azure Files storage redundancy for WVD profiles: LRS vs ZRS vs GRS](azure-files-storage-redundancy-lrs-zrs-grs-2.md)
- [Azure high-availability building blocks](azure-high-availability-building-blocks.md)
- [Don't make the management tool highly available, spend the budget on compute and storage](dont-make-nerdio-manager-highly-available.md)
- [Don't Spend Budget Making the AVD Management Tool Highly Available](dont-make-the-avd-management-plane-highly-available.md)
- [DR/HA Discovery Questions for AVD and Nerdio](dr-ha-discovery-questions-avd.md)
- [Active/Active DR for AVD Across Two Regions](nerdio-active-active-dr.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [WVD high availability: what you actually own vs what Microsoft owns](wvd-high-availability-architecture.md)
