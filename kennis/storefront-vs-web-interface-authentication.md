---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, web-interface, authentication, delivery-controller]
layer: reference
bron: inside-citrix-fma
---

# StoreFront vs Web Interface user authentication

StoreFront has its own integral authentication service. Users can authenticate via username/password, domain pass-through, NetScaler pass-through, smart cards, or unauthenticated access. The StoreFront authentication service picks up credentials and authenticates them with a domain controller. Once authenticated, StoreFront forwards credentials as an XML query to a configured Delivery Controller (assuming at least two are configured); meanwhile it checks its local datastore for existing subscriptions and stores them in memory. The receiving Delivery Controller then contacts a domain controller again to validate the user before responding to StoreFront.

Web Interface works differently: it has no internal authentication service, so it immediately forwards credentials as an XML query to a Delivery Controller, where a domain controller authenticates the user before responding. Web Interface can authenticate users to and enumerate/aggregate resources from multiple XenApp Farms and XenDesktop Sites, but with no App Controller.

As of StoreFront 3.0, Citrix reintroduced XML-based authentication: running a few PowerShell scripts makes authentication fall back to the XenDesktop/XenApp XML service (as with Web Interface), useful when StoreFront is not in the same domain as XenDesktop/XenApp or when no AD trust is possible. Disabled by default. As of StoreFront 3.5, PowerShell is no longer needed; it can be toggled directly from the StoreFront management console.

## Verwante notities

- [Bas's distinction: authentication versus verification](authentication-vs-verification-distinction.md)
- [Broker Service: XML, STA and the Principal Broker](broker-service-xml-sta-principal.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
- [StoreFront 2.0 replaces Web Interface (key features)](storefront-2-replaces-web-interface.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront over Web Interface, and StoreFront design notes](storefront-over-web-interface.md)
- [StoreFront authenticates locally, Web Interface delegates via XML](storefront-vs-webinterface-auth-flow.md)
- [XenApp Services URLs for legacy Receiver access](xenapp-services-urls-legacy-access.md)
