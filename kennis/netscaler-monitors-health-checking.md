---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, monitor, load-balancing, health-check]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler monitors: why load balancing needs health checks

Load balancing on the NetScaler happens at the virtual server / service object level. Without health checking, if a back-end service goes down (e.g. its server crashed) and the virtual server doesn't know, it keeps load balancing requests to a dead service, producing 404s (resource not available).

A monitor is a logical object that sits between the service and server object (bound to the service object) and constantly checks the health and availability of the back-end systems and the services on them. This is how it worked around 2015, but the concept of pairing load balancing with active health monitoring is durable.

*Bron: blogpost 'Citrix NetScaler basics: VIPs, service/server objects and monitors' (2015-08-03), basvankaam.com.*

## Verwante notities

- [NetScaler content switching: one entry point, many back ends](netscaler-content-switching-basics.md)
- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [NetScaler SNIP, MIP and static routes: how traffic is sourced and routed](netscaler-snip-mip-static-routes.md)
- [NetScaler 10.1 TFTP load balancing for PVS boot HA](netscaler-tftp-load-balancing-pvs.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
- [Teaching stance: master the basics before the advanced NetScaler features](netscaler-walk-before-you-run-teaching.md)
