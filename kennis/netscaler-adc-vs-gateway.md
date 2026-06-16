---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, adc, gateway, licensing, remote-access]
layer: reference
bron: inside-citrix-fma
---

# NetScaler ADC vs NetScaler Gateway

The NetScaler is considered an optional FMA component but rarely absent from a full-blown Citrix environment — often called Citrix's 'Swiss Army knife' for handling inbound and outbound traffic. The Gateway functionality is the best-known edition, but it is only about 5–10% of what the appliance can do; NetScalers are often deployed at large scale in environments that don't even include XenDesktop/XenApp.

**Citrix NetScaler** refers to the **Application Delivery Controller (ADC)** product line, capable of load balancing and HA, content switching, application offloading/SSL offload, application firewalling, cloud connectivity, hybrid cloud and more. The **NetScaler Gateway** (formerly Citrix Access Gateway / CAG) is primarily for secure remote access to XenDesktop/XenApp. You essentially buy a normal NetScaler and a Gateway license limits it to Gateway functionality. There's significant overlap between the two — it comes down to which license you upload, with the Gateway license being the most basic. The ADC edition also has Gateway functionality built in. The Gateway sits in the DMZ between the internet and the corporate LAN, fronted by firewalls. (Bas recommends Marius Sandbu's NetScaler books.)

## How it worked then (NetScaler 10.5 era, 2014)

The same distinction held in the NetScaler 10.5 era: Citrix NetScaler = the ADC line; NetScaler Gateway (formerly CAG) = primarily secure remote access. You buy a normal NetScaler but a Gateway license limits it to Gateway functionality, while ADCs can do far more — load balancing and HA, content switching, SSL offload, application firewalling, cloud and hybrid-cloud connectivity.

*Bron: blogpost 'Citrix NetScaler Gateway, the basics!' (2014-09-23), basvankaam.com.*

## Verwante notities

- [NetScaler ADC vs Gateway: same box, different license](netscaler-adc-vs-gateway-licensing.md)
- [NetScaler appliance models: VPX, MPX, SDX, CPX](netscaler-appliance-models-vpx-mpx-sdx-cpx.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [NetScaler HDX Proxy announced to replace the Secure Gateway (Synergy 2016)](netscaler-hdx-proxy-replaces-secure-gateway.md)
- [NetScaler platforms, editions and HA](netscaler-platforms-and-licensing.md)
