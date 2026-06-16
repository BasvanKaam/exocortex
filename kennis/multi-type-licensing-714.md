---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, licensing, delivery-group, powershell]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Multi-type licensing in XenDesktop/XenApp 7.14

Version 7.14 introduced multi-type licensing: you can mix **consumption models** (User/Device and Concurrent) within the same Site, configured per Delivery Group. Before 7.14 this required separate Sites.

Key constraint: **editions cannot be mixed** within a Site. Enterprise and Platinum licenses still need separate Sites, regardless of consumption model. The Site edition is enforced to be equal across all Delivery Groups.

The feature is disabled by default and at the time could only be enabled per Delivery Group via PowerShell, using Get/Set/New-BrokerDesktopGroup with -ProductCode (XDT or MPS) and -LicenseModel (UserDevice or Concurrent). A DG without multi-type enabled inherits the Site license info from initial setup.

How it worked then in 7.14.

*Bron: blogpost 'XenDesktop & XenApp 7.14 multi-type licensing - what it is, how it works and what to be aware of' (2017-06-12), basvankaam.com.*

## Verwante notities

- [Citrix license type vs edition vs consumption model](citrix-license-type-vs-edition.md)
- [Citrix license types: user, device and concurrent](citrix-license-types-user-device-concurrent.md)
- [Platinum grows in worth, but unbundle the editions](platinum-worth-it-and-unbundle-editions.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [How the Citrix license server allocates user/device licenses](user-device-license-server-allocation.md)
- [XenDesktop 7 editions and licensing models](xendesktop7-editions-and-licensing.md)
