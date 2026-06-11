---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, high-availability, storefront, delivery-controller, design]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# One is none: always deploy two StoreFronts and two Delivery Controllers

How it worked then (Citrix 7.x): StoreFront is on the critical path for authentication, enumeration and launch, so a single StoreFront outage stops users launching resources (a direct ICA connection is the only, non-recommended, exception). Hence 'one is none', always deploy at least two StoreFront servers per Site behind a load balancer (NetScaler or Windows NLB) so failure is invisible. Same logic for Delivery Controllers: configure at least two on StoreFront, giving active/passive failover by default. For high-logon-load orgs, go active/active by load-balancing the DC connections, either on the NetScaler or by StoreFront's own built-in mechanism (pre-3.5 via editing web.config loadBalance=on/off, 3.5+ via a GUI checkbox under Manage Delivery Controllers; the built-in LB behaves like RRDNS). The redundancy principle is durable even though the products are EOL.

*Bron: blogpost 'Web Interface & StoreFront XML-based authentication' (2017-05-01), basvankaam.com.*

## Verwante notities

- [GSLB selection metrics and the Metric Exchange Protocol](netscaler-gslb-metrics-mep.md)
- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
- [StoreFront 2.0 replaces Web Interface (key features)](storefront-2-replaces-web-interface.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [StoreFront over Web Interface is a good thing (April 2013)](storefront-over-web-interface-call.md)
- [XenDesktop 7.6 HA options before Zones](xendesktop-76-ha-options-pre-zones.md)
