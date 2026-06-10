---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, web-interface, design, multi-site]
layer: rich
bron: inside-citrix-fma
---

# StoreFront over Web Interface, and StoreFront design notes

Bas recommends StoreFront for new and existing deployments — Web Interface is end-of-life (June 2018), while StoreFront is built for the future with features Web Interface lacks. Email-based discovery, for example, requires StoreFront.

Design pointers he gives:
- Deploy at least one StoreFront server per Zone (needed in case of a WAN link failure).
- There are two authentication points in a Site: StoreFront and NetScaler (NetScaler optional). As of StoreFront 3.0 the XML service can also authenticate users.
- User subscriptions sync between all StoreFront servers in the same server group.
- When editing the web.conf file, work on only one StoreFront server at a time (preferably the first one installed/configured), then propagate changes.
- Multi-site lets you map user groups to a preferred site and configure a Recovery site that sits idle until all other deployments stop accepting connections.
- If only a single desktop is published, StoreFront auto-launches it after login (changeable via web.conf, see CTX139058).

## Verwante notities

- [Desktop Appliance sites for non-domain-joined machines](desktop-appliance-sites.md)
- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
- [Bas's StoreFront chapter key takeaways](storefront-chapter-key-takeaways.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront vs Web Interface user authentication](storefront-vs-web-interface-authentication.md)
- [XenApp Services URLs for legacy Receiver access](xenapp-services-urls-legacy-access.md)
