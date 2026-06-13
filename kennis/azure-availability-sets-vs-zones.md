---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure, high-availability, availability-zones, fault-domain]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Azure Availability Sets vs Availability Zones

Availability Set = a local (single-datacenter) redundancy construct. VMs are spread across fault domains and update domains within one Azure datacenter. A fault domain is a logical group of hardware sharing a common power source and network switch (like a rack); ARM deployments spread VMs across up to three fault domains by default. An update domain is a group that can be rebooted/maintained together; five non-user-configurable update domains are assigned by default, with a sixth VM wrapping back to the first. A set limits the blast radius of a single hardware/power/network failure but all data stays in one datacenter.

Availability Zone = protection against a whole-datacenter failure. Zones are distinct physical locations within a region, each with independent power, cooling and networking. Enabled regions have a minimum of three zones (not all regions support zones). Zones in a region are typically 20-50 miles apart, joined by very fast links. Spreading 3+ VMs across 3 zones gives 3 fault and 3 update domains, one per datacenter.

SLA: 99.99% VM uptime when two or more VMs are deployed across two or more Availability Zones in a region. Using Sets or Zones is itself free of charge; you don't duplicate VMs.

*Bron: blogpost 'How to Make Your 1,000+ User WVD Deployment Highly Available' (2020-12-07), basvankaam.com.*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [Azure Files storage redundancy for WVD profiles: LRS vs ZRS vs GRS](azure-files-storage-redundancy-lrs-zrs-grs-2.md)
- [Azure high-availability building blocks](azure-high-availability-building-blocks.md)
- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [Nerdio shines where Microsoft's WVD HA docs are missing](nerdio-fills-microsoft-wvd-ha-doc-gap.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
