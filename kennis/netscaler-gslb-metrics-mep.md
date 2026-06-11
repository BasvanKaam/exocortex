---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [netscaler, gslb, mep, rtt, static-proximity, load-balancing]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# GSLB selection metrics and the Metric Exchange Protocol

How it worked then. GSLB site selection can use Round Robin, Least Connection, Least Bandwidth, Source IP Hash, random and more. Static Proximity binds users to a specific site. RTT (Round Trip Time) measures the distance between the local NetScaler and the originating DNS server to pick the closest site, improving user experience.

MEP (Metric Exchange Protocol) is the proprietary protocol NetScalers use to exchange site metrics, network metrics and persistence information between GSLB sites, so load-balancing decisions can be made. MEP also detects availability: if a NetScaler becomes unreachable, traffic is automatically routed to the still-active site (useful in a DR Gateway setup).

Design note Bas flags: also consider where the user data lives and whether both sites are equally configured. In DR scenarios it's common to offer only business-critical/core apps, and to remember that multiple active DFSR targets are not supported.

*Bron: blogpost 'Citrix NetScaler… The basics continued, part five. Global Server Load Balancing' (2015-10-20), basvankaam.com.*

## Verwante notities

- [NetScaler GSLB is DNS-based multi-site traffic management](netscaler-gslb-dns-foundation.md)
- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- [One is none: always deploy two StoreFronts and two Delivery Controllers](one-is-none-storefront-dc-redundancy.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [Multi-site brokering is easy, user-data locality is the catch](user-data-locality-is-the-catch-in-multisite.md)
