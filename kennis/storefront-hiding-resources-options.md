---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [storefront, citrix, xenapp, xendesktop, delivery-group, powershell]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Options for hiding published resources in StoreFront / XenApp

How it worked with StoreFront 3.0 (2015). By default every member of a Delivery Group sees all resources in that group. Ways to hide resources, each with trade-offs:

- **Multiple Delivery Groups**: one per resource or group of resources, with a subset of users each. Helps delegated administration but can sprout many groups and complicate day-to-day admin. A session host can only belong to one Delivery Group, so you may need extra machines.
- **Limited Visibility**: per-application, per-user within a Delivery Group. Simple. Only works for applications, not published desktops. The app stays hidden even when accessed from within a published desktop, and it can still be launched from the actual Windows machine (just hidden, not blocked).
- **Delivery Group Access Policies (needs NetScaler) and Exclusion Filters (PowerShell)**: applied at Delivery Group level, so all-or-nothing for that group. Effectively forces you into multiple Delivery Groups.
- **StoreFront SDK filters (PowerShell)**: applied at store level, by resource type or by keyword. Work for both apps and desktops, but once hidden a resource is hidden for everybody (no per-user control). Requires loading the StoreFront SDK modules on the StoreFront server, the XenDesktop modules (Add-PSSnapin Citrix*) on the Delivery Controller, and RemoteSigned execution policy on both.

*Bron: blogpost 'Citrix StoreFront: hiding resources across two stores' (2015-08-05), basvankaam.com.*

## Verwante notities

- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [Hiding apps (Limit Visibility) vs hiding desktops (PowerShell entitlement filter)](limit-visibility-vs-entitlement.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [StoreFront resource subscription and Keywords](storefront-resource-subscription-keywords.md)
- [StoreFront subscriptions, Self Service Store and Keywords](storefront-subscriptions-and-keywords.md)
