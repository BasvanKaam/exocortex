---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, ssl-offload, dmz, security]
layer: reference
bron: inside-citrix-fma
---

# NetScaler SSL offloading and DMZ placement

The device offloading SSL traffic — the NetScaler — can live in the **DMZ**, while the web servers it offloads for sit safely on the more secure internal network. Because the NetScaler can authenticate users (when applicable) and check, inspect, decrypt and re-encrypt all traffic before it reaches the web server, the internal connections stay safe.

Beyond SSL offloading, the NetScaler also does SSL and TCP multiplexing and supports HTTP caching, compression and front-end optimizations to make web applications more responsive.

## Verwante notities

- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler appliance models: VPX, MPX, SDX, CPX](netscaler-appliance-models-vpx-mpx-sdx-cpx.md)
- [NetScaler IP addresses: NSIP, SNIP and MIP](netscaler-ip-addresses-nsip-snip-mip.md)
- [NetScaler platforms, editions and HA](netscaler-platforms-and-licensing.md)
- [NetScaler SSL certificates and certificate trust](netscaler-ssl-certificates-and-trust.md)
- [NetScaler static routes](netscaler-static-routes.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [Securing StoreFront connections with SSL and NetScaler](securing-storefront-connections-with-ssl.md)
