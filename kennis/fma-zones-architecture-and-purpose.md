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
