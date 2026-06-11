---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [storefront, receiver, unified-experience, x1, branding]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Enabling the Unified Receiver Experience in StoreFront 3.0

How it worked then (2015, StoreFront 3.0 / Receiver 4.3 "X1"): the upgrade itself was trivial (download, install, next a few times) and preserved existing config - both stores, PowerShell-hidden apps, single sign-on, and Receiver settings survived. The one thing Bas had to redo was removing the "HDX file access" splash on the published desktop (an HKLM registry setting on the client, wiped by installing the new 4.3 Receiver). To switch on the new look you had to do it in the right order: first go to "Receiver for Web", select the store, and "Disable Classic Receiver Experience" (this affects only web users, not natively installed Receiver). Only then could you go to "Stores" and "Set Unified Experience as Default" - doing it the other way around throws an error. After disabling Classic, you gained "Customise Receiver Appearance" for Logon branding (the web login page) and Header branding (the store post-login), plus "Manage Featured App Groups" for grouping resources by category.

*Bron: blogpost 'How to: Upgrading and configuring StoreFront 3.0 - The Unified Experience!' (2015-07-02), basvankaam.com.*

## Verwante notities

- [Companies overspend on StoreFront branding](branding-storefront-overrated-effort.md)
- [Citrix Summit 2015: Receiver X1, Framehawk, XenMobile 10](citrix-summit-2015-announcements.md)
- [Time to finally let go of Web Interface and consolidate Receiver](finally-let-go-of-web-interface.md)
- [Receiver platforms and the Receiver X1](receiver-platforms-and-x1.md)
- [StoreFront 2.0 replaces Web Interface (key features)](storefront-2-replaces-web-interface.md)
- [StoreFront resource subscription and Keywords](storefront-resource-subscription-keywords.md)
