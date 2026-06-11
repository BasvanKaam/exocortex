---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [storefront, multi-site, fma, user-mapping, failover, netscaler, citrix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# StoreFront Multi-Site aggregation, mapping and failover

How it worked then (StoreFront 2.0 / XenDesktop 7): by default StoreFront enumerates all apps and desktops from every configured Site/Farm (XenDesktop, XenApp, VIAB controllers). If a resource exists in multiple Sites the user sees duplicate icons. Multi-Site config fixes this and adds resilience:

- Aggregation: identical resources (same name and path, matching characteristics) across Sites/Farms are presented as a single icon; StoreFront picks the best instance based on server availability, existing sessions and your configured order. AppController apps cannot be aggregated.
- User Mapping: route users to a specific deployment based on AD group membership (like IMA zone-preference policies); group A to Site A, group B to Site B, each Site acting as the other's failover.
- Load balance: spread connections randomly across controllers (active/active needs 2+ StoreFront servers plus NetScaler; otherwise active/passive with one server).
- Subscription synchronization: keep user app subscriptions in sync across server groups (stores must share the same name and be in the same/trusted AD domain).
- Optimal NetScaler Gateway: define the preferred appliance per deployment so cross-location launches don't needlessly traverse the WAN.

All of this is configured in the web.config file (C:\inetpub\wwwroot\Citrix\storename\), effective immediately, and breaks StoreFront if misconfigured.

*Bron: blogpost 'Configure StoreFront Multi-Site configurations' (2013-12-02), basvankaam.com.*

## Verwante notities

- [Critique: why isn't this in the GUI? (web.config friction)](build-it-into-the-gui-position.md)
- [App subscriptions are stored by the platform, not the client](client-vs-platform-subscriptions-gotcha.md)
- [NetScaler GSLB is DNS-based multi-site traffic management](netscaler-gslb-dns-foundation.md)
- [GSLB selection metrics and the Metric Exchange Protocol](netscaler-gslb-metrics-mep.md)
- [One is none: always deploy two StoreFronts and two Delivery Controllers](one-is-none-storefront-dc-redundancy.md)
- [StoreFront's powerful features shouldn't be locked behind web.config](storefront-config-should-be-in-the-gui.md)
- [StoreFront high availability and Delivery Controller load balancing](storefront-ha-and-load-balancing.md)
- [Options for hiding published resources in StoreFront / XenApp](storefront-hiding-resources-options.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront features configured via web.config](storefront-webconfig-configuration.md)
- [Multi-site brokering is easy, user-data locality is the catch](user-data-locality-is-the-catch-in-multisite.md)
- [VMware Cloud Pod Architecture aggregates pods behind one entitlement layer](vmware-cloud-pod-architecture.md)
