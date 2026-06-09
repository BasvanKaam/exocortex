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
