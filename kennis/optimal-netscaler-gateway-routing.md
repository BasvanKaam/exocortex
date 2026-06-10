---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [netscaler, gateway, routing, storefront, ica, wan]
layer: reference
bron: inside-citrix-fma
---

# Optimal NetScaler Gateway routing

When deployments (Sites) each have their own NetScaler, StoreFront lets you define the optimal/preferred NetScaler appliance for accessing each deployment.

Problem it solves: if a store aggregates resources from two geographically separated locations, each with a NetScaler Gateway, a user connecting through the Gateway in location A can launch a resource in location B, but by default the connection is routed back through the Gateway they originally connected to, traversing the corporate WAN.

FMA fact: Optimal NetScaler Gateway routing changes this, routing the user's ICA traffic through the most applicable NetScaler (the one connecting them to their actual XenDesktop Site), even if the initial connection came through a different NetScaler. NetScaler can also load balance StoreFront-to-Controller connections and NetScaler-to-StoreFront connections.

## Verwante notities

- [Beacon-based Receiver connection routing](beacon-based-receiver-connection-routing.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [External launch process: Hosted Shared Desktop via NetScaler](external-launch-process-hsd-netscaler.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [NetScaler vServers, service objects and server objects](netscaler-virtual-server-service-server-objects.md)
- [The Secure Ticket Authority (STA)](secure-ticket-authority-sta.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
