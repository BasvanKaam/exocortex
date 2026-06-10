---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, vserver, load-balancing, monitor]
layer: reference
bron: inside-citrix-fma
---

# NetScaler vServers, service objects and server objects

The NetScaler uses **virtual servers (vServers)** — logical objects — to deliver services (secure gateway, load balancing, content switching, VPN, etc.); you'll typically have several at once. A vServer is the first point of contact for external users (usually behind a firewall): the external connection terminates here. It has a **VIP** (virtual IP, known externally), a name (for administration), and a defined protocol and port.

A **service object** represents an application running on a back-end system (e.g. HTTP). You give it a name, tell it the protocol and port, and which back-end server to forward requests to; it is then **bound** to the vServer. A **server object** points to the IP address or FQDN of the actual back-end system (one per back-end web server) and is bound to the service object.

Chain: vServer (VIP, name, protocol, port) → bound to service object → bound to server object → points to the real back-end server.

**Monitors:** load balancing happens at the vServer/service-object level. A monitor is a logical object bound to the service object that continuously checks back-end health. When a back-end or its service becomes unresponsive, the monitor marks the service down in the console and stops sending traffic, preventing 404 errors from being load-balanced to dead services.

## Verwante notities

- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler appliance models: VPX, MPX, SDX, CPX](netscaler-appliance-models-vpx-mpx-sdx-cpx.md)
- [NetScaler high availability and clustering](netscaler-high-availability-clustering.md)
- [NetScaler IP addresses: NSIP, SNIP and MIP](netscaler-ip-addresses-nsip-snip-mip.md)
- [NetScaler static routes](netscaler-static-routes.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [Optimal NetScaler Gateway routing](optimal-netscaler-gateway-routing.md)
- [StoreFront high availability and Delivery Controller load balancing](storefront-ha-and-load-balancing.md)
