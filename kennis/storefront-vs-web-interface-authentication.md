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
