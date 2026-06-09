---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [zones, vda-registration, delivery-controller, failover, primary-zone]
layer: reference
bron: inside-citrix-fma
---

# FMA Zones VDA registration and Controller failover

VDA registration behavior in Zones:
- VDAs automatically register with a Delivery Controller in their own Zone (preferred Controller). If none are available, they register with a Controller in the primary Zone, and stay registered there even when a local Controller comes back online. There is no fallback mechanism (at least not today).
- When a Machine Catalog is moved between Zones, its registered VDAs re-register with the new Zone's Controller.
- VDAs in the primary Zone only register with a Controller in the primary Zone.

Controller failover:
- If a Zone Delivery Controller fails, another in the same Zone takes over. If none are available, it auto-fails-over to a Controller in the primary Zone (consistent with VDAs registering in the primary Zone when no local Controllers are available).

Keep Machine Catalogs close to any host connection they use; one or multiple host connections can be added per Zone.

Brokering requests from a satellite Zone can be limited via the Registry key HKLM\Software\Citrix\DesktopServer\ThrottledRequestAddressMaxConcurrentTransactions, set per Delivery Controller. If the key does not exist, no limit is enforced.
