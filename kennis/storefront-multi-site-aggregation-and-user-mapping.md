---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, multi-site, aggregation, user-mapping, recovery-site]
layer: reference
bron: inside-citrix-fma
---

# StoreFront multi-Site: aggregation, user mapping and recovery sites

By default StoreFront enumerates resources from all configured Sites/Farms (XenDesktop, XenApp and/or VDI-in-a-Box Controllers). Adding Controllers from another Site auto-enumerates those resources, but if the same app/desktop exists on multiple Sites the user sees duplicate icons. StoreFront multi-Site configurations solve this with aggregation: when a resource is available from multiple Sites/Farms, StoreFront presents all instances as a single icon. For aggregation the desktops/apps must have the exact same name, path and all other characteristics on each server; deployments need not be identical otherwise. XenMobile App Controller apps cannot be aggregated.

When a user launches an aggregated resource, StoreFront picks the most appropriate Controller instance based on server availability, whether the user already has an active session, and your configured ordering.

Multi-Site also enables HA deployments: load balancing, failover, or a non-active disaster-recovery Site. User Mapping grants access to a specific deployment based on AD group membership (like the old Zone preference policies), letting you offer different resources per Site while aggregating through one Store; users see only what their permissions allow. Without user mapping a multi-Site setup is active/passive (active/active needs 2+ StoreFront servers plus a NetScaler). A Recovery Site is another XenDesktop/XenApp Site that sits idle (passive) until all primary Sites become unreachable.

Prior to StoreFront 3.5 all of this was configured manually in web.config; as of 3.5 options such as User Mapping and resource aggregation are available directly from the GUI.

## Verwante notities

- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [Optimal NetScaler Gateway routing](optimal-netscaler-gateway-routing.md)
- [How StoreFront and XenMobile App Controller aggregated apps via a trust](storefront-appcontroller-trust-aggregation.md)
- [Bas's StoreFront chapter key takeaways](storefront-chapter-key-takeaways.md)
- [StoreFront's powerful features shouldn't be locked behind web.config](storefront-config-should-be-in-the-gui.md)
- [StoreFront high availability and Delivery Controller load balancing](storefront-ha-and-load-balancing.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [StoreFront over Web Interface, and StoreFront design notes](storefront-over-web-interface.md)
- [StoreFront subscription storage, server groups and synchronization](storefront-subscription-storage-and-sync.md)
- [StoreFront vs Web Interface user authentication](storefront-vs-web-interface-authentication.md)
- [StoreFront features configured via web.config](storefront-webconfig-configuration.md)
- [VMware Cloud Pod Architecture aggregates pods behind one entitlement layer](vmware-cloud-pod-architecture.md)
