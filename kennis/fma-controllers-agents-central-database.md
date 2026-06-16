---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, xendesktop7, architecture, delivery-controller]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# FMA architecture: Controllers, Agents and a critical central database (durable)

The FlexCast Management Architecture is made up of Delivery Controllers and Delivery Agents. Agents are installed on every physical/virtual machine and register with the Controllers and license server; Controllers talk to a central SQL database. That database holds both configuration (Site policies, Machine Catalogs, Delivery Groups, published apps/desktops) and all live runtime data (who is connected to what, server load, connection state) used for load-balancing decisions.

Critical consequence Bas stresses: if the database is unreachable, running sessions keep working, but new sessions can't be established and configuration changes aren't possible - so build in database redundancy (SQL replication or clustering). This Controller/Agent/central-DB shape and its database-availability failure mode is the durable foundation that underpinned Citrix Virtual Apps and Desktops for years.

*Bron: blogpost 'FlexCast Management Architecture' (2013-05-28), basvankaam.com.*

## Verwante notities

- [The Central Site database in the FMA](central-site-database-fma.md)
- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [FMA core components: Receiver, StoreFront, NetScaler Gateway](fma-core-components-overview.md)
- [The FMA core services and how they communicate](fma-services-complete-overview.md)
- [FMA service high availability via peer service groups](fma-services-high-availability.md)
- [FMA services run independently, with separate DB connection strings](fma-services-independent-registry-accounts.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [The VDA: client-side component, services and registration](vda-overview-services-and-registration.md)
