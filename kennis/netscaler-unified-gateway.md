---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, unified-gateway, content-switching]
layer: reference
bron: inside-citrix-fma
---

# NetScaler Unified Gateway

Introduced with the NetScaler 11.0 release, the **Unified Gateway** is a single vServer that receives all inbound traffic and routes it to the appropriate internal virtual servers bound to it, letting you reach multiple back-end services through a single IP address / URL. The underlying technologies aren't new (it reuses Content Switching, Client Access and Bookmarks), but it adds benefits. The Unified Gateway vServer can be paired with a NetScaler Gateway vServer for secure remote access and with one or more load-balancing vServers.

Advantages:
- A single IP/URL to reach XenDesktop/XenApp apps and desktops, XenMobile-hosted mobile and web apps, and cloud resources — freeing up extra IP addresses.
- All NetScaler and XenDesktop features applied on one platform: Single Sign-on, HDX and NetScaler Insight Services, End Point Analysis, RDP proxy, Content Switching, Smart Access Control, etc.
- Triple-A (AAA) support, allowing integration with Office 365 and SSO against existing NetScaler load-balance servers.

You can configure as many Unified Gateway vServers as needed. Bas advises considering it for larger, more complex environments.

## Verwante notities

- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler IP addresses: NSIP, SNIP and MIP](netscaler-ip-addresses-nsip-snip-mip.md)
- [NetScaler SSL certificates and certificate trust](netscaler-ssl-certificates-and-trust.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [NetScaler vServers, service objects and server objects](netscaler-virtual-server-service-server-objects.md)
- [Optimal NetScaler Gateway routing](optimal-netscaler-gateway-routing.md)
