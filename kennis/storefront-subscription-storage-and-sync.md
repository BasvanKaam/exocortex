---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, subscription, ese, server-groups, synchronization]
layer: reference
bron: inside-citrix-fma
---

# StoreFront subscription storage, server groups and synchronization

Subscriptions must be stored so users don't re-subscribe every login. Prior to StoreFront 2.x a separate external database was needed; now StoreFront uses the Windows Extensible Storage Engine (the same technology behind Microsoft Access and Exchange) to store and index subscription info locally.

StoreFront servers are grouped into server groups; locally stored subscription info is automatically replicated peer-to-peer to other servers in the same group, making subscriptions highly available.

Subscription synchronization: if users connect to StoreFront servers in different deployments/server groups with access to similar resources, periodic synchronization of subscriptions between stores in different server groups avoids re-subscribing. Requirements: all stores must have the same name, and all server groups must reside in the AD domain of the users' accounts or a trusted domain.

Each store has its own independent subscription datastore. It is common to create two stores (internal and external), which means subscriptions would be stored twice and users subscribe twice, unless you configure the two stores to share a common subscription database (by editing web.config), so subscriptions are identical regardless of internal/external access.

## Verwante notities

- [Self Service Store vs Mandatory Store and shortcut-only mode](self-service-vs-mandatory-store.md)
- [Bas's StoreFront chapter key takeaways](storefront-chapter-key-takeaways.md)
- [StoreFront high availability and Delivery Controller load balancing](storefront-ha-and-load-balancing.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront resource subscription and Keywords](storefront-resource-subscription-keywords.md)
- [StoreFront subscriptions, Self Service Store and Keywords](storefront-subscriptions-and-keywords.md)
