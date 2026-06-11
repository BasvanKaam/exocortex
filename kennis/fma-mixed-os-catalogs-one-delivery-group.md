---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, machine-catalog, delivery-group, xenapp]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FMA lets one Delivery Group span Catalogs with different OSes (2013 feature)

A headline FMA change: all Agents communicate with the same Controller regardless of installed OS, which lets a single Delivery Group be assigned to multiple different Machine Catalogs. For XenApp this was big - a classic XenApp Farm required identical OSes across all servers, but in XD7 you could have one Catalog on Server 2008 R2 and another on Server 2012 and publish separate hosted shared desktops from one Delivery Group, all in the same infrastructure. The Delivery Controller (former Data Collector) also no longer needed Terminal Services installed. Also new in this release: MCS could now provision server workloads, not just desktops.

*Bron: blogpost 'FlexCast Management Architecture' (2013-05-28), basvankaam.com.*

## Verwante notities

- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [Excalibur's Catalog + Delivery Group model (how XD7 worked at launch)](excalibur-catalogs-delivery-groups-model.md)
- [Delivering five Windows generations from one infrastructure](five-generations-of-windows-one-infrastructure.md)
- [Delivering Linux shared hosted desktops: controller, catalog and delivery group setup](linux-vda-controller-and-catalog-config.md)
