---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, zones, xendesktop-7-7, satellite-zone, primary-zone, fma, multi-site]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenDesktop 7.7 Zones: satellite sub-Sites without their own HA SQL

How it worked then (XenApp/XenDesktop 7.7, Jan 2016): traditionally, multiple geographically separated locations meant multiple separate Sites, each needing its own highly available SQL central Site database, managed separately. Zones brought a middle ground: each satellite zone is essentially a sub-Site but without needing its own HA SQL database. You always have one Primary Site (renameable) and optionally multiple zones. Citrix Studio is configured only in the Primary Site and manages every zone from there (Studio and Director can be published to zones). Each zone has at least its own Delivery Controller, StoreFront server, optionally NetScaler, and one or more VDAs. The goal: connect users to the resources closest to them, keeping traffic local. Delivery Controllers in zones communicate directly with the central Site database and license server in the Primary zone. These are not the old XenApp 6.5 IMA zones, but close, and they brought zones to XenDesktop for the first time.

*Bron: blogpost 'How to configure zones in XenDesktop and XenApp 7.7 plus some extra's!' (2016-01-05), basvankaam.com.*

## Verwante notities

- [New FMA features land in Citrix Workspace Cloud first, then on-prem](positie-zones-and-cloud-first-feature-flow.md)
- [VMware Cloud Pod Architecture aggregates pods behind one entitlement layer](vmware-cloud-pod-architecture.md)
