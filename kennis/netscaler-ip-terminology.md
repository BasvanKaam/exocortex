---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, networking, nsip, snip, vip, fundamentals]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer

How it worked then:

- vServer (virtual server): delivers a service; you can run multiple independent vServers on one NetScaler (gateway, load balancing, SSL offload, etc.).
- NSIP (NetScaler IP): the management IP. Mandatory, only one, can't be removed, requires a reboot to change.
- SNIP (Subnet IP): used for server-side connections to directly-connected subnets. With USNIP mode (on by default) it becomes the source address to the internal network; adds a route to the routing table; not mandatory; multiple SNIPs on one subnet are used round-robin.
- MIP (Mapped IP): like SNIP, used when no SNIP is available or USNIP is disabled.
- VIP (Virtual IP): the address of a vServer that end users connect to. Never used as a source IP, so it isn't involved in back-end communication (SNIP/MIP handle that).

*Bron: blogpost 'Citrix NetScaler Gateway, the basics!' (2014-09-23), basvankaam.com.*

## Verwante notities

- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler content switching: one entry point, many back ends](netscaler-content-switching-basics.md)
- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- [Intranet Applications: the subnet objects that define split tunneling](netscaler-intranet-applications-object.md)
- [NetScaler monitors: why load balancing needs health checks](netscaler-monitors-health-checking.md)
- [NetScaler SNIP, MIP and static routes: how traffic is sourced and routed](netscaler-snip-mip-static-routes.md)
- [NetScaler split tunneling: route only corporate traffic through the VPN](netscaler-split-tunneling-concept.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
- [Teaching stance: master the basics before the advanced NetScaler features](netscaler-walk-before-you-run-teaching.md)
- [Inspecting prerequisites up front saves the whole deployment](prerequisites-discipline-saves-time.md)
