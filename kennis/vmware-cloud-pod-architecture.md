---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vmware, horizon, cloud-pod, multi-site, architecture]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VMware Cloud Pod Architecture aggregates pods behind one entitlement layer

How it worked then (Horizon 7 era, 2017): a traditional Horizon/View deployment is one or more Pods, each Pod up to five View blocks, each Pod up to 10,000 desktops (2,000 per block). The problem with multiple Pods is each must be managed as a separate entity with its own entitlements, with no native way to aggregate across them. Cloud Pod Architecture (a 'Pod Federation') fixes this: it publishes a single icon that load-balances across pools/pods/sites and centralizes management through a single global entitlement layer. Assignment modes: nearest site (non-persistent), a bound Home site (persistent, governed by a FromHome true/false policy controlling where the desktop search starts), or multi-site assignment for HA/DR. Search order is local Pod first, then same site, then all sites. Limits at the time: 25 Pods, 5 sites, 172 Connection Servers, 75,000 users. Inter-site coordination runs over a Global Data Layer (topology, policies, entitlements) plus the View InterPod API (VIPA) for find/launch and health status. Bas explicitly frames it as VMware's answer to what Citrix does with StoreFront multi-site aggregation / zone-preference policies.

*Bron: blogpost 'VMware Cloud Pod Architecture explained' (2017-05-07), basvankaam.com.*

## Verwante notities

- [How VMware Blast Extreme worked (Horizon 7 era)](blast-extreme-protocol-internals.md)
- [NetScaler GSLB is DNS-based multi-site traffic management](netscaler-gslb-dns-foundation.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [Multi-site brokering is easy, user-data locality is the catch](user-data-locality-is-the-catch-in-multisite.md)
- [How VMware Instant Clones (vmFork) provision desktops in seconds](vmware-instant-clones-vmfork-mechanics.md)
- [XenDesktop 7.7 Zones: satellite sub-Sites without their own HA SQL](xendesktop-77-zones-satellite-sub-sites.md)
