---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, snip, mip, static-route, networking, routing]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler SNIP, MIP and static routes: how traffic is sourced and routed

How it worked on the NetScaler around 2015.

- **SNIP (Subnet IP)**: comparable to a layer-3 routing table entry. Configuring a SNIP automatically adds a route to the NetScaler's routing table for that directly-connected subnet/VLAN. One SNIP per directly-connected subnet. When traffic is routed via a SNIP, the source IP of the packets becomes that SNIP. SNIPs only work for directly reachable subnets. By default a SNIP is not bound to a specific interface (traffic goes out all interfaces, hub-like) but can be bound via VLANs. A SNIP is not mandatory.
- **Default route**: acts as the NetScaler's default gateway. With no known internal route (SNIP/MIP) for received traffic, it sends everything out the default route, back toward the internet.
- **USNIP (Use Subnet IP)**: enabled by default. If disabled, no SNIPs are used as source.
- **MIP (Mapped IP)**: used as the source IP when USNIP is disabled or no SNIP is available, or alongside a SNIP on the same subnet. A MIP only adds a route to the table if it is the first address on the subnet.
- **Static route**: needed when a subnet (e.g. subnet D) is not directly reachable but must be reached through an intermediate subnet (A) connected to a router. You 'add route' telling the NetScaler to send traffic for D via the router interface on subnet A. Adding a SNIP for a non-directly-connected subnet won't work.

*Bron: blogpost 'Citrix NetScaler basics part two: static routes, SNIP and MIP' (2015-08-18), basvankaam.com.*

## Verwante notities

- [Intranet Applications: the subnet objects that define split tunneling](netscaler-intranet-applications-object.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [NetScaler monitors: why load balancing needs health checks](netscaler-monitors-health-checking.md)
- [NetScaler split tunneling: route only corporate traffic through the VPN](netscaler-split-tunneling-concept.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
- [Teaching stance: master the basics before the advanced NetScaler features](netscaler-walk-before-you-run-teaching.md)
