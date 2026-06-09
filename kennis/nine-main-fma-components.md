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
