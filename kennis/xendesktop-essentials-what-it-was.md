---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop-essentials, azure, citrix-cloud, licensing]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix XenDesktop Essentials: what it was and what the price covered

How it worked then (March 2017): XenDesktop Essentials was a Citrix Cloud service born from the Citrix-Microsoft partnership that let you buy Windows 10 virtual desktops from the Azure Marketplace. It was unlocked by a change to Microsoft's Windows 10 Product Use Rights (PUR), which had previously barred Windows desktops from multi-tenant cloud platforms.

Key facts: Windows 10 desktops only (no Windows 7/8, no Linux, no Hosted Shared Desktops). Restricted to Microsoft Enterprise Agreement customers with active Software Assurance and per-user Windows 10 Enterprise licenses, delivering Windows 10 CBB (Current Branch for Business). Price was 12 USD per user per month, minimum 25 users, pay-as-you-go, auto-renewing, no discounts (unlike the annually-billed Citrix Cloud XenApp/XenDesktop services). Background provisioning used Machine Creation Services (MCS), not PVS.

The 12 USD covered only the Citrix Cloud management plane (Studio, Director, Delivery Controllers, SQL, underlying OS and Azure infra, 24x7 support). You brought your own Azure subscription, your own Windows 10 licenses, and paid all Azure IaaS (compute, storage, network) separately.

*Bron: blogpost 'Citrix XenDesktop Essentials - all facts listed!' (2017-03-02), basvankaam.com.*

## Verwante notities

- ['Finally' one bill, but the 25-user minimum rules out small shops](citrix-managed-desktop-finally-one-bill.md)
- [The key line between Essentials and full Citrix Cloud: VDA placement](essentials-vs-full-citrix-cloud-vda-placement.md)
