---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, components, site, active-directory]
layer: reference
bron: inside-citrix-fma
---

# The nine main FMA components and the XenDesktop Site definition

From a high-level perspective the FMA is built around nine main components:
1. Delivery Controller
2. Virtual Delivery Agent
3. StoreFront
4. Central Site database
5. Receiver
6. Studio
7. Director
8. License server
9. Host Connection

A XenDesktop/XenApp Site is where all main and subcomponents reside: it encompasses all Delivery Controllers, VDAs, Host Connections and everything needed to host and virtualize desktops and applications, managed as a single entity from Citrix Studio.

FMA fact: Active Directory is required for authentication and authorization of users in a Citrix environment, and this includes DNS.

## Verwante notities

- [The XenDesktop Central Site database](central-site-database-role.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [The evolution of the FlexCast Management Architecture](evolution-of-the-fma.md)
- [The four most prominent FMA core services](fma-four-prominent-core-services.md)
- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
- [Bas's case for why deep FMA knowledge still matters in the cloud era](why-fma-knowledge-still-matters-relevance.md)
