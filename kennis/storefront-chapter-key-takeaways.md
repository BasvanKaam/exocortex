---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, key-takeaways, self-service-store, mandatory-store, keywords]
layer: rich
bron: inside-citrix-fma
---

# Bas's StoreFront chapter key takeaways

Bas's own summary list closing the StoreFront chapter:

- There are two points of authentication within a XenDesktop/XenApp Site: StoreFront and NetScaler.
- With Zones, always deploy at least one StoreFront server per Zone, needed in case of WAN link failure.
- Users may need to subscribe to resources they are allowed to start. These subscriptions sync across all StoreFront servers in the same server group.
- This is the 'Self Service Store' setup, enabled by default. It can be disabled, leaving the 'Mandatory Store' configuration where all permitted resources display by default, no subscriptions needed.
- Combined with Self Service, Keywords (configured in Studio) can auto-subscribe users to certain resources, like a standard desktop.
- With email-based discovery you can either advertise the Store or hide it (user configures Receiver themselves via setup URL or provisioning file).
- When editing web.conf, do it on only one StoreFront server at a time, preferably the first one installed. Changes can be manually propagated to other servers in the group.
- Multi-site deployments can map user groups to a preferred site and configure a Recovery site that sits idle until all other deployments stop accepting connections.
- If only a single desktop is published, StoreFront auto-launches it after login; change via web.conf (CTX139058).
- StoreFront is key for Receiver pass-through authentication / Single Sign-on (CTX200157).

## Verwante notities

- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [Self Service Store vs Mandatory Store and shortcut-only mode](self-service-vs-mandatory-store.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront over Web Interface, and StoreFront design notes](storefront-over-web-interface.md)
- [StoreFront resource subscription and Keywords](storefront-resource-subscription-keywords.md)
- [StoreFront server sizing and supported OSes](storefront-server-sizing.md)
- [StoreFront subscription storage, server groups and synchronization](storefront-subscription-storage-and-sync.md)
- [StoreFront subscriptions, Self Service Store and Keywords](storefront-subscriptions-and-keywords.md)
