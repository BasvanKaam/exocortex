---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, desktop-appliance-sites, non-domain-joined, netscaler]
layer: reference
bron: inside-citrix-fma
---

# Desktop Appliance sites for non-domain-joined machines

Users with non-domain-joined desktop machines can access their desktops through Desktop Appliance sites. Non-domain-joined here means devices not joined to a domain within the Microsoft Active Directory forest containing the StoreFront servers.

Like the XenApp Services URL, when you create a new store for a XenDesktop deployment using Citrix Studio, a Desktop Appliance site is created for the store by default.

Important: if you are connecting through a NetScaler Gateway you cannot access a Desktop Appliance site. External connections from outside the network are not supported, period. Also ensure the right version of Receiver is installed.
