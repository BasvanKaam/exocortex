---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [high-availability, delivery-controller, one-is-none, principles]
layer: rich
bron: inside-citrix-fma
---

# The 'one is none' rule and Delivery Controller high availability

Bas leans on the IT adage 'one is none' as a recurring design principle (an FMA fact: 'Your environment is as strong as its weakest link. Make sure to apply the one is none rule wherever and whenever it makes sense.').

Applied to Delivery Controllers: if the only server hosting the Delivery Controller role is unavailable, users cannot be authenticated/verified and cannot launch desktops or apps. Therefore deploy at least two Delivery Controllers per Site, on different physical hosts when virtualized, to avoid a single point of failure. All online Controllers actively participate in handling session requests; if one goes offline, another takes over automatically and instantly. All Controllers in a Site share the same Central Site database and are therefore equally configured.

His design tips (key takeaways): virtualize Controllers for flexibility; keep them physically close to the database server and Host Connections; a minimum of one Controller per Zone is needed in case of a WAN link failure; StoreFront can be configured with a NetScaler load-balance VIP to spread connections across the Controllers.

## Bron-citaten (NL, verbatim)

> Your environment is as strong as its weakest link. Make sure to apply the 'one is none' rule wherever and whenever it makes sense.

## Verwante notities

- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [Connection Leasing failover behavior and limitations](connection-leasing-failover-behavior.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [Delivery Controller as the heart of the FMA](delivery-controller-is-heart-of-fma.md)
- [Delivery Controller server sizing and supported OS](delivery-controller-sizing.md)
- [FMA architecture: Controllers, Agents and a critical central database (durable)](fma-controllers-agents-central-database.md)
- [FMA service high availability via peer service groups](fma-services-high-availability.md)
- [NetScaler high availability and clustering](netscaler-high-availability-clustering.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
- [StoreFront high availability and Delivery Controller load balancing](storefront-ha-and-load-balancing.md)
- [VDA high-availability mode (direct ICA, last resort)](vda-high-availability-mode.md)
