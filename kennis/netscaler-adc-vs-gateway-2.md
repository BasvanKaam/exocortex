---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, gateway, adc, remote-access, citrix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler ADC vs NetScaler Gateway editions

How it worked then (NetScaler 10.5 era, 2014): Citrix NetScaler = the Application Delivery Controller (ADC) line; NetScaler Gateway (formerly Citrix Access Gateway, CAG) = primarily secure remote access. You buy a normal NetScaler but a Gateway license limits it to Gateway functionality.

ADCs can do far more than remote access: load balancing and HA, content switching, SSL offload, application firewalling, cloud and hybrid-cloud connectivity. The ADC edition also has Gateway functionality built in. The Gateway sits in the DMZ between the internet and the corporate LAN, fronted by firewalls.

*Bron: blogpost 'Citrix NetScaler Gateway, the basics!' (2014-09-23), basvankaam.com.*

## Verwante notities

- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [NetScaler 10.5 made ICA proxy built-in and unlimited](netscaler-105-ica-proxy-built-in.md)
- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler ADC vs Gateway: same box, different license](netscaler-adc-vs-gateway-licensing.md)
- [NetScaler appliance models: VPX, MPX, SDX, CPX](netscaler-appliance-models-vpx-mpx-sdx-cpx.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
