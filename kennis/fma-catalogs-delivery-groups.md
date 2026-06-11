---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, fma, machine-catalog, delivery-group, publishing]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Machine Catalogs vs Delivery Groups in the FMA

How it worked in XenDesktop/XenApp 7.x (Flex Management Architecture): when XenApp merged into XenDesktop's FMA, resource publishing moved from the old XenApp model to Catalogs and Delivery Groups.

- Machine Catalogs hold the machines from which resources (applications and/or desktops) are published.
- Delivery Groups (DGs) take some or all machines out of a Catalog, auto-discover installed applications by talking to the VDA, and let you assign those resources to users individually or by AD group.
- A machine can only be a member of one Delivery Group (and one Catalog) at a time. To publish per-application or per-small-group with separate DGs, you also need separate Catalogs, which can balloon the number of objects.
- Provisioning method (PVS, MCS, App-V) is independent of access: without assigning users, resources stay unreachable however they were provisioned.

Bas initially described the membership rule slightly wrong and corrected it in the comments: one Catalog can feed multiple DGs (each DG getting a different machine), but a single machine still belongs to one DG at a time.

*Bron: blogpost 'Configuring Citrix XenDesktop 7.x Desktop publishing and Limited Visibility!' (2014-06-26), basvankaam.com.*

## Verwante notities

- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [Excalibur's Catalog + Delivery Group model (how XD7 worked at launch)](excalibur-catalogs-delivery-groups-model.md)
