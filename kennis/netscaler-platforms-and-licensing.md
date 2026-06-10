---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [netscaler, mpx, vpx, high-availability, licensing]
layer: reference
bron: inside-citrix-fma
---

# NetScaler platforms, editions and HA

NetScalers come as physical (MPX, SDX), virtual (VPX), virtual-on-physical (VPX on SDX) and containerised (CPX, Citrix's containerised NetScaler, in tech preview, mainly for test/dev). All are nearly equal in features; the license you upload unlocks functionality — 'Pay as you Grow'. Physical appliances differ mainly in compute and the Cavium SSL accelerator card (more powerful card = more SSL transactions).

Capacity: the virtual VPX handles up to 1500 concurrent ICA connections (Citrix-supported); for more you move to a physical MPX, which depending on model handles 10,000 to 35,000 concurrent ICA connections.

There are three ADC platform licenses (Standard, Enterprise, Platinum) plus a separate NetScaler Gateway license and a universal license; every normal ADC license already includes Gateway functionality. A free NetScaler VPX Express edition exists (same features as VPX standard, but no SSL Offload, max 5 Mbps, licensed per year). HA (2 nodes) is active-passive via heartbeat with failover; both appliances must be the same make/model, software version and licenses. Clustering (active/active using ECMP) scales up to 32 nodes.

## Verwante notities

- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler appliance models: VPX, MPX, SDX, CPX](netscaler-appliance-models-vpx-mpx-sdx-cpx.md)
- [NetScaler high availability and clustering](netscaler-high-availability-clustering.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
