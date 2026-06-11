---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, excalibur, machine-catalog, delivery-group, mcs, xenapp]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Machine Catalogs and Delivery Groups: mixed-OS flexibility

How it worked then (2013). Excalibur introduced two concepts that reshaped how machines map to users:

- **Machine Catalog** — a collection of virtual/physical machines managed as one entity sharing a common master image. Used for hosted shared apps/desktops (XenApp-style) or dedicated/pooled virtual desktops (XenDesktop-style). Roughly the XenApp 'Worker Group' equivalent, with a key difference below.
- **Delivery Group** (formerly Desktop Group) — a flexible way of allocating machines from one or more Catalogs to users who need a common set of resources and the same experience (policies, profiles, personal storage).

The headline change: in classic XenApp every server in a Farm/Worker Group had to share the same OS. In Excalibur you can create one Catalog on Windows Server 2008R2 and another on Server 2012 and publish separate hosted shared desktops within the same infrastructure. And a single Delivery Group can be assigned across multiple *different* Catalogs, simplifying management. This mixed-OS capability, made possible by Delivery Agents, was the practical 'big new feature.'

Because XenApp Sites are now managed from Studio, **MCS** can create XenApp Catalogs too (not just XenDesktop), with creation wizards guiding the initial Site roll-out. PVS is unchanged.

*Bron: blogpost 'Project Avalon... Excalibur! Part one' (2013-02-13), basvankaam.com.*

## Verwante notities

- [Excalibur's Catalog + Delivery Group model (how XD7 worked at launch)](excalibur-catalogs-delivery-groups-model.md)
- [Early bullish take on Excalibur: impressive, simplified, the right direction](excalibur-impressed-early-take.md)
- [Excalibur merges XenApp and XenDesktop onto FMA](excalibur-merges-xenapp-xendesktop-fma.md)
- [Delivering five Windows generations from one infrastructure](five-generations-of-windows-one-infrastructure.md)
- [Machine Catalogs vs Delivery Groups in the FMA](fma-catalogs-delivery-groups.md)
- [FMA lets one Delivery Group span Catalogs with different OSes (2013 feature)](fma-mixed-os-catalogs-one-delivery-group.md)
- [FMA multi-OS and mixed Machine Catalog support vs IMA](fma-multi-os-support-vs-ima.md)
- [Hiding apps (Limit Visibility) vs hiding desktops (PowerShell entitlement filter)](limit-visibility-vs-entitlement.md)
- [Options for hiding published resources in StoreFront / XenApp](storefront-hiding-resources-options.md)
- [XenApp roles removed/replaced moving to Excalibur (2013 mapping)](xenapp-roles-removed-or-replaced-in-excalibur.md)
