---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenapp, fma, sql-express, netscaler-vpx, small-deployments]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# A supported all-in-one XenApp box: Delivery Controller + StoreFront + VDA + SQL Express

How it worked then (XenApp/XenDesktop 7.x, 2016): you can install the Virtual Delivery Agent (VDA) on the same machine as the Delivery Controller, StoreFront and the SQL Express database, and Citrix fully supports this combined setup. Free, supported building blocks for a low-cost small Site:
- SQL Express: free, supported, selectable when installing the first Delivery Controller. No HA, but fine for smaller Sites, even with MCS provisioning.
- NetScaler VPX Express: free, supported, same capabilities (including HA) as the paid MPX/VPX with a few limits.
- XenServer as a free hypervisor (included vGPU and Intel Iris Pro driver support).
- MCS for workload provisioning, built into Studio/the FMA, no separate infrastructure.

Resilience without SQL HA came from Connection Leasing (7.6) and the reworked Local Host Cache, which supplement SQL Always-on and keep users connected when the central Site database is unreachable.

*Bron: blogpost 'Citrix XenApp single machine setup - Cheap, fast and supported!' (2016-07-12), basvankaam.com.*

## Verwante notities

- [NetScaler HDX Proxy announced to replace the Secure Gateway (Synergy 2016)](netscaler-hdx-proxy-replaces-secure-gateway.md)
