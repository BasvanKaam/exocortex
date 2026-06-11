---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, authentication, fma, concept]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Authentication vs verification are two distinct steps

A recurring distinction Bas drills throughout the FMA: authentication and verification are not the same thing. Authentication is making sure somebody is who they claim to be. Verification (or validation) is done to find out which resources are assigned to that user, primarily based on Active Directory group memberships. The names blur in everyday talk but the two operations happen separately, and in a Citrix flow they even hit a domain controller at different points (StoreFront authenticates, the Delivery Controller validates). A durable mental model for any access architecture, not just Citrix.

*Bron: blogpost '100+ Citrix XenApp & XenDesktop FMA facts listed' (2017-04-11), basvankaam.com.*

## Verwante notities

- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [StoreFront authenticates locally, Web Interface delegates via XML](storefront-vs-webinterface-auth-flow.md)
