---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [wvd, avd, high-availability, availability-zones, azure-files, architecture, explainer]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# WVD high availability: what you actually own vs what Microsoft owns

Bas's architectural mental model for making a large (1000+ user) WVD deployment highly available. Useful as a clean framing of the division of responsibility.

**Microsoft owns:** the WVD control plane (database, web portal, brokering, load balancing). You don't update it or make it HA, Microsoft does. Nothing for you to do there.

**You own:** your VMs and your data (user profiles, departmental and personal data). That's the whole scope of WVD HA work.

**Availability Sets (local-datacenter redundancy):**
- Spread VMs across fault domains (logical group sharing power source + network switch, like a rack) and update domains (logical group that can be maintained/rebooted together).
- Default for ARM WVD deployments: up to 3 fault domains, 5 non-configurable update domains. A failure or update hits only a subset of VMs.
- All data still lives in one datacenter. Think of Availability Sets as protection against rack-level / hardware failure within a single datacenter.

**Availability Zones (datacenter-level redundancy):**
- Unique physical locations within a region, each with independent power, cooling, networking. Minimum 3 zones per enabled region, usually 20-50 miles apart, connected by very fast links.
- Spreading 3+ VMs across 3 zones distributes them across 3 fault and 3 update domains, one per zone. Think of Zones as protection against datacenter-level failure.
- 99.99% VM uptime SLA when 2+ VMs are deployed across 2+ zones in a region.

**Cost note:** Availability Sets and Zones themselves are free and don't duplicate VMs. The cost is egress data between VMs in different zones (cross-zone VM data-transfer billing started Feb 2021), and cross-region transfer for GEO redundancy.

Note (dated): Microsoft at the time published no WVD-specific Availability Zones guidance, so community PowerShell posts filled the gap. Nerdio Manager exposed Zones per-hostpool and Sets deployment-wide via checkboxes.

*Bron: Nerdio-content 'Making your 1000+ user WVD deployment highly available!' (Blogs).*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [Cloud is more reliable than on-prem, be realistic](cloud-is-more-reliable-than-on-prem.md)
- [Cloud is still more reliable than on-prem, be realistic about it](cloud-still-more-reliable-than-on-prem.md)
- [Disaster recovery for WVD: keep machines off until needed](wvd-disaster-recovery-cost-angle.md)
