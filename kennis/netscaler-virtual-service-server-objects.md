---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, citrix, adc, load-balancing, networking]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler binding chain: virtual server to service to server object

How it worked on the Citrix NetScaler (ADC) around 2015. The virtual server is the first point of contact from the outside (a firewall usually sits in front). It terminates the external connection and has a VIP (virtual IP, known on the outside), a name for administration, and a defined protocol and port.

The configuration is a chain of bound logical objects:
- Virtual server (VIP, name, protocol, port) is bound to a service object.
- A service object represents an application running on a back-end system (e.g. HTTP for web requests). It defines protocol/port and which back-end server requests are forwarded to.
- The service object is bound to a server object, which points to the IP address or FQDN of the actual back-end system. One server object per back-end web server.

This chain is the foundation; the same object model applies whether the virtual server is for gateway, load balancing, content switching or VPN.

*Bron: blogpost 'Citrix NetScaler basics: VIPs, service/server objects and monitors' (2015-08-03), basvankaam.com.*

## Verwante notities

- [NetScaler content switching: one entry point, many back ends](netscaler-content-switching-basics.md)
- [Content switching policy types and Unified Gateway](netscaler-cs-policy-types-and-unified-gateway.md)
- [NetScaler GSLB is DNS-based multi-site traffic management](netscaler-gslb-dns-foundation.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [NetScaler monitors: why load balancing needs health checks](netscaler-monitors-health-checking.md)
- [NetScaler SNIP, MIP and static routes: how traffic is sourced and routed](netscaler-snip-mip-static-routes.md)
- [NetScaler SSL offload, wildcard and SAN certs](netscaler-ssl-offload-and-cert-types.md)
- [NetScaler 10.1 TFTP load balancing for PVS boot HA](netscaler-tftp-load-balancing-pvs.md)
- [Teaching stance: master the basics before the advanced NetScaler features](netscaler-walk-before-you-run-teaching.md)
