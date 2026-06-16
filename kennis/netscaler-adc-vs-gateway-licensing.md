---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, netscaler, adc, gateway, licensing, vpx, mpx, sdx]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler ADC vs Gateway: same box, different license

How it worked around NetScaler 10.x (2014):

- NetScaler ADC = Application Delivery Controller (load balancing, HA, content switching, app firewall, offload, cloud connectivity). NetScaler Gateway (formerly Citrix Access Gateway / CAG) = primarily secure remote access (SSL proxy).
- All NetScalers, physical or virtual, are hardware-identical in capability. What you can do is unlocked by the edition/platform license you upload: Standard, Enterprise, or Platinum.
- Form factors: VPX = virtual appliance on your hypervisor; MPX = physical appliance; SDX = physical appliance that runs multiple VPX instances (up to 40 in 2014; doubled to 80 with 10.5) on a branded XenServer.
- 'Pay as you grow': upgrade by purchasing and uploading a higher edition license file, no hardware swap.
- Universal licenses (optional) enable advanced Gateway features (full SSL VPN, SmartAccess endpoint analysis, clientless access, Micro VPN for XenMobile) for a set number of concurrent users.
- Burst Pack licenses temporarily raise throughput to absorb traffic spikes without new hardware.
- ADC NetScalers include Gateway functionality by default; buying an ADC license just for remote access is wasteful since Gateway licenses are cheaper.

*Bron: blogpost 'Citrix NetScaler (10.5) licensing. What's new with Access Gateway!' (2014-07-01), basvankaam.com.*

## Verwante notities

- [Credit to Citrix for simplifying NetScaler licensing without a price grab](citrix-simplifying-licensing-praise.md)
- [NetScaler 10.5 made ICA proxy built-in and unlimited](netscaler-105-ica-proxy-built-in.md)
- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler appliance models: VPX, MPX, SDX, CPX](netscaler-appliance-models-vpx-mpx-sdx-cpx.md)
- [NetScaler platforms, editions and HA](netscaler-platforms-and-licensing.md)
- [Teaching stance: master the basics before the advanced NetScaler features](netscaler-walk-before-you-run-teaching.md)
