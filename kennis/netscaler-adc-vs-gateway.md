---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, adc, gateway, licensing]
layer: reference
bron: inside-citrix-fma
---

# NetScaler ADC vs NetScaler Gateway

The NetScaler is considered an optional FMA component but rarely absent from a full-blown Citrix environment — often called Citrix's 'Swiss Army knife' for handling inbound and outbound traffic. The Gateway functionality is the best-known edition, but it is only about 5–10% of what the appliance can do; NetScalers are often deployed at large scale in environments that don't even include XenDesktop/XenApp.

**Citrix NetScaler** refers to the **Application Delivery Controller (ADC)** product line, capable of load balancing and HA, content switching, application offloading, application firewalling, cloud connectivity, hybrid cloud and more. The **NetScaler Gateway** (formerly Citrix Access Gateway / CAG) is primarily for secure remote access to XenDesktop/XenApp. You essentially buy a normal NetScaler with limited functionality by uploading a Gateway license. There's significant overlap between the two — it comes down to which license you upload, with the Gateway license being the most basic. (Bas recommends Marius Sandbu's NetScaler books.)

## Verwante notities

- [CVE-2019-19781 Citrix ADC / SD-WAN vulnerability (2020 context)](cve-2019-19781-citrix-adc.md)
- [Community resources: Team RGE and Marius Sandbu's NetScaler e-Book](euc-community-resources-teamrge-msandbu.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
- [NetScaler ADC vs NetScaler Gateway editions](netscaler-adc-vs-gateway-2.md)
- [NetScaler appliance models: VPX, MPX, SDX, CPX](netscaler-appliance-models-vpx-mpx-sdx-cpx.md)
- [NetScaler platforms, editions and HA](netscaler-platforms-and-licensing.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [NetScaler vServers, service objects and server objects](netscaler-virtual-server-service-server-objects.md)
