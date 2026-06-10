---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [zones, satellite-zones, primary-zone, central-site-database, connection-leasing]
layer: reference
bron: inside-citrix-fma
---

# FMA Zones: architecture and purpose

Zones returned in the FMA via a phased approach (this is phase one), now applying to both XenDesktop and XenApp. Unlike IMA Zones, FMA Zones still depend on the Central Site database (there is no LHC).

The problem Zones solve: in the early FMA, servicing geographically separated locations required separate Sites, each with its own HA SQL setup and full configuration, making management complex. Zones let you configure up to ten satellite Zones under a primary Zone (which holds the HA SQL setup), managing all Zones as a single Site from Citrix Studio with a single SQL HA setup. All Zone-related static and dynamic data is stored in the same Central Site database.

Key points:
- Each satellite Zone is essentially a sub-Site without its own highly available SQL database, but still needs at least one Delivery Controller and one StoreFront server (one is enough, though not recommended), plus optional NetScaler and one or more VDAs.
- Zones connect users to the closest resources, keeping traffic local. Traffic flows as usual, with Zone Delivery Controllers communicating directly with the Central Site database and license server in the primary Zone.
- Delivery Controllers in the primary Zone store leasing info for all Zones; satellite-Zone Controllers store leasing info only for the primary Zone and their own.
- New features arrive first in CWC (Citrix Workspace Cloud, including XenApp and XenDesktop as the Applications and Desktops service) before on-premises; Zones were tested in CWC first.
- Provisioning Services is not 'Zone aware'; configure Machine Catalogs by hand in Studio (otherwise PVS Catalogs default to the primary Zone).

## Verwante notities

- [The XenDesktop Central Site database](central-site-database-role.md)
- [FMA architectural casualties: Zones, LHC and Worker Groups removed then re-added](fma-architectural-changes-zones-lhc-removed.md)
- [FMA Zones VDA registration and Controller failover](fma-zones-vda-registration-and-failover.md)
- [Host Connection key takeaways: MCS/PVS and cloud support](host-connection-mcs-pvs-cloud-support-key-takeaways.md)
- [Host Connections now support cloud, not just hypervisors](host-connections-cloud-support.md)
- [IMA Zones vs. FMA Zones comparison](ima-zones-vs-fma-zones-comparison.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [Bas's Studio and Zones chapter key takeaways](studio-zones-chapter-key-takeaways.md)
- [Zone connection quality limits (bandwidth and RTT)](zone-connection-quality-limits.md)
- [Zones in the FMA are not the same as IMA 6.5 Zones](zones-fma-vs-ima.md)
