---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, high-availability, load-balancing, netscaler, rrdns]
layer: reference
bron: inside-citrix-fma
---

# StoreFront high availability and Delivery Controller load balancing

StoreFront is vital for authentication, enumeration and launch; with no StoreFront available users cannot launch resources (a direct ICA connection is the only exception, not recommended). So deploy at least two StoreFront servers per Site, fronted by a load balancer (NetScaler or Windows NLB) so users don't notice a server failure.

StoreFront must be configured with at least one Delivery Controller (FQDN or IP); following 'one is none', configure at least two. On Controller failure, StoreFront automatically fails over to the next Controller, an active/passive configuration. For high logon loads, an active/active approach fits better, achieved with a NetScaler or by letting StoreFront itself load balance connections to the Controllers.

Up to StoreFront 3.5 you edited web.config manually, e.g. the farm line with loadBalance="on"/"off". As of StoreFront 3.5 this is a GUI checkmark under 'Manage Delivery Controllers'. The built-in LB mechanism is based on (or produces a result similar to) RRDNS technology.

## Verwante notities

- [CWC StoreFront hosting options](cwc-storefront-options.md)
- [FMA service high availability via peer service groups](fma-services-high-availability.md)
- [NetScaler high availability and clustering](netscaler-high-availability-clustering.md)
- [NetScaler vServers, service objects and server objects](netscaler-virtual-server-service-server-objects.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [StoreFront server sizing and supported OSes](storefront-server-sizing.md)
- [StoreFront subscription storage, server groups and synchronization](storefront-subscription-storage-and-sync.md)
