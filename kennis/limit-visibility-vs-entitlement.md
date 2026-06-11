---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, limit-visibility, powershell, entitlement-policy]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Hiding apps (Limit Visibility) vs hiding desktops (PowerShell entitlement filter)

How it worked in XenDesktop 7.x:

- The Limit Visibility feature is per application: 'Limit visibility for this application to the users listed below' hides the icon from everyone else. It does NOT work on published desktops.
- Hiding an icon does not prevent launch. To truly block access, move the app into a separate Delivery Group without it, or lock down the Hosted Shared Desktop.
- To restrict a published desktop in a 'Desktops and Applications' Delivery Group: Studio creates one Entitlement Policy Rule and one App Entitlement Policy Rule, both available to all DG users with no exposed user filter. Use PowerShell to scope the desktop to a specific AD group:

```
Add-PSSnapin Citrix*
Get-BrokerEntitlementPolicyRule
Set-BrokerEntitlementPolicyRule -Name "<Delivery Group>" -AddIncludedUsers "Domain\<AD group>" -IncludedUserFilterEnabled $true
```

This sets IncludeUserFilterEnabled to True and binds an AD group, so only that group sees the published desktop while apps in the same DG can be governed separately via Limit Visibility.

*Bron: blogpost 'Configuring Citrix XenDesktop 7.x Desktop publishing and Limited Visibility!' (2014-06-26), basvankaam.com.*

## Verwante notities

- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [Don't buy a desktop management suite just to lock down a desktop](management-suites-only-if-used-fully.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [How share and NTFS permissions combine](share-vs-ntfs-permission-combination.md)
- [Options for hiding published resources in StoreFront / XenApp](storefront-hiding-resources-options.md)
- [Everything you do in Studio is PowerShell underneath](studio-is-powershell-underneath.md)
- [XenDesktop 7 delegated administration: roles, scopes, objects](xd7-delegated-administration-roles-scopes-objects.md)
