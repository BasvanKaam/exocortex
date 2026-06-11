---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, storefront, web-interface, authentication, xml]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# StoreFront authenticates locally, Web Interface delegates via XML

How it worked then (2017, XenApp/XenDesktop 7.x): StoreFront ships with its own authentication service that talks directly to Active Directory, so it authenticates the user itself, then forwards credentials as an XML query to a Delivery Controller (which re-validates against a DC) to find out which resources are assigned. Web Interface has no internal authentication service: it immediately forwards credentials as an XML query to the Delivery Controller, which authenticates the user against a domain controller. This is the 'XML-based user authentication' model. As of StoreFront 3.0 Citrix re-introduced XML-based auth as a fallback option (PowerShell to enable up to 3.5, GUI thereafter), useful when StoreFront is in a different domain than XenApp/XenDesktop and no AD trust is possible. The 6-step internal flow (authenticate at StoreFront, forward to DC, DC validates against AD, DC checks Central Site DB for assigned resources, return to StoreFront, render icons) is the durable mental model even if the products are gone.

*Bron: blogpost 'Web Interface & StoreFront XML-based authentication' (2017-05-01), basvankaam.com.*

## Verwante notities

- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [Authentication vs verification are two distinct steps](fma-authentication-vs-verification.md)
- [ICA connection renamed HDX connection (terminology shift, 2013)](ica-connection-becomes-hdx-connection.md)
- [StoreFront 2.0 replaces Web Interface (key features)](storefront-2-replaces-web-interface.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
- [StoreFront vs Web Interface user authentication](storefront-vs-web-interface-authentication.md)
- [Keep Web Interface when migrating, choose StoreFront when greenfield (April 2013)](web-interface-vs-storefront-migration-call.md)
