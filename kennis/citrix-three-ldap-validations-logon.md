---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, authentication, ldap, netscaler, storefront, broker-service]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# A Citrix external logon validates against LDAP three times

In the classic XenApp/XenDesktop (FMA) external logon flow, the same user is validated against Active Directory three separate times, and these are not the same operation:

1. Through NetScaler (session cookie) to AD, after which the credentials are redirected to StoreFront.
2. Through StoreFront, either via the StoreFront Authentication Service or via StoreFront to the XML service on a Delivery Controller, to AD. This is where the authentication token is actually built.
3. Through the XML/Broker service (validation) to AD, to discover the security group SIDs used for resource enumeration.

Key nuance Bas highlights: authentication (building the token) and validation (finding the group SIDs for enumeration) are distinct steps that happen to both hit AD. How it worked then, on XenApp/XenDesktop 7.x with NetScaler Gateway in front.

*Bron: blogpost 'Demystifying the Citrix XenApp logon, enumeration and launch steps' (2016-12-19), basvankaam.com.*

## Verwante notities

- [The Broker Service bundles brokering, XML and STA in one process](citrix-broker-service-three-roles.md)
- [The STA only comes into play when traffic traverses a NetScaler](citrix-sta-only-with-netscaler.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [Authentication vs verification are two distinct steps](fma-authentication-vs-verification.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
- [StoreFront authenticates locally, Web Interface delegates via XML](storefront-vs-webinterface-auth-flow.md)
