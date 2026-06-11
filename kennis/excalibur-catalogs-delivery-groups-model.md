---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, excalibur, xendesktop7, machine-catalog, delivery-group]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Excalibur's Catalog + Delivery Group model (how XD7 worked at launch)

In the Excalibur (XenDesktop 7) Tech Preview the build order is: create a Site, then Machine Catalogs holding the physical or virtual machines, then Delivery Groups that reference those Catalogs. There are two kinds of Delivery Group: a Desktop Delivery Group (VDI, typically Desktop-OS catalogs, users assigned to the group) and an Application Delivery Group (published apps and hosted desktops, typically Server-OS catalogs, where users are added during the app-publishing process rather than to the group itself).

Machine Catalogs based on VMs require a configured Host Infrastructure (a connection to XenServer/vCenter/SCVMM); without one, only physical machines can be added. Delivery Agents (DA) replace the old way of installing XenApp and must be baked into the image / master image for MCS or PVS.

*Bron: blogpost 'Project Avalon... Excalibur! Part two' (2013-04-08), basvankaam.com.*

## Verwante notities

- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [Intelligent Configuration Validation and built-in Profile Management](excalibur-built-in-config-validation.md)
- [Excalibur merges XenApp and XenDesktop onto FMA](excalibur-merges-xenapp-xendesktop-fma.md)
- [Machine Catalogs vs Delivery Groups in the FMA](fma-catalogs-delivery-groups.md)
- [FMA lets one Delivery Group span Catalogs with different OSes (2013 feature)](fma-mixed-os-catalogs-one-delivery-group.md)
- [FMA Server VDA vs Desktop VDA: multi-session and direct controller comms](fma-server-vda-vs-desktop-vda.md)
- [Citrix Studio console root nodes](studio-console-root-nodes.md)
