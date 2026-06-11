---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, excalibur, fma, xenapp, xendesktop, ima, architecture]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Excalibur merges XenApp and XenDesktop onto FMA

How it worked then (2013, Tech Preview). Excalibur (the first release of Project Avalon, later shipping as XenDesktop 7) merged XenApp and XenDesktop into a single product, console and architecture. XenApp's capabilities were re-delivered through the XenDesktop infrastructure, meaning hosted shared apps/desktops now ran on the same FlexCast Management Architecture (FMA) as virtual desktops.

The big architectural break for XenApp: **IMA is gone**, replaced by FMA. Concretely:
- Data store moves to Microsoft SQL Server (Express possible); Access and Oracle no longer supported. HA via SQL clustering/mirroring or hypervisor HA.
- No more IMA service or protocol; no Data Collectors (load spreads evenly across all Controllers in the Site); no Terminal Services on the Controller.
- A 'Farm' is now a 'Site.'
- Servers join via **Delivery Agents** (DAs, the XenDesktop VDA concept extended to XenApp), so no full XenApp install is needed on each server. One server DA, one desktop DA, both talking to the same Delivery Controller.
- Single management console (**Citrix Studio**) for everything; the old Shadow Taskbar is replaced by **Director** (which also does shadowing).

This is the conceptual foundation of every modern Citrix CVAD architecture; the FMA-over-IMA shift is the durable takeaway even though the product names are dated.

*Bron: blogpost 'Project Avalon... Excalibur! Part one' (2013-02-13), basvankaam.com.*

## Verwante notities

- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [Citrix 2013 solutions-focused certification structure](citrix-2013-certification-program-structure.md)
- [Citrix Project Accelerator as a guided design tool](citrix-project-accelerator-tool.md)
- [Intelligent Configuration Validation and built-in Profile Management](excalibur-built-in-config-validation.md)
- [Excalibur's Catalog + Delivery Group model (how XD7 worked at launch)](excalibur-catalogs-delivery-groups-model.md)
- [Excalibur drops Citrix Profiling (app streaming) for App-V (2013 Synergy news)](excalibur-drops-profiling-for-appv.md)
- [Early bullish take on Excalibur: impressive, simplified, the right direction](excalibur-impressed-early-take.md)
- [Excalibur is XenDesktop on steroids and here to stay (April 2013)](excalibur-is-here-to-stay.md)
- [FMA Server VDA vs Desktop VDA: multi-session and direct controller comms](fma-server-vda-vs-desktop-vda.md)
- [FMA unified XenApp and XenDesktop on one architecture](fma-shared-xenapp-xendesktop.md)
- [FMA vs IMA: no Zones, no Data Collectors, no Local Host Cache (2013)](fma-vs-ima-no-zones-no-lhc.md)
- [IMA-to-FMA terminology: Farm to Site, Data Collector to Delivery Controller](ima-to-fma-terminology-map.md)
- [Positie: Citrix was inexplicably late adding delegated admin to XenDesktop](positie-citrix-late-with-xendesktop-delegated-admin.md)
- [Server 2012 .NET 3.5 Feature on Demand install gotcha (how it worked then)](server-2012-net35-feature-on-demand-gotcha.md)
- [XenApp folded into the FMA: the Excalibur / XenDesktop 7.0 moment](xenapp-joins-fma-excalibur-2013.md)
