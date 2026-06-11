---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [linux-vda, delivery-controller, machine-catalog, delivery-group, hdx, citrix-studio]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Delivering Linux shared hosted desktops: controller, catalog and delivery group setup

How it worked then (2015, guest content by Mick Glover): to broker Linux VDA sessions you first had to update every Site Controller by running the Update-BrokerServiceConfig.ps1 script (from citrix-linuxvda-scripts-1.0.0.zip) after loading the FMA snap-ins with 'asnp citrix*'. The script rewrote BrokerService.exe.Config (under C:\Program Files\Citrix\Broker\Service) with the WCF endpoints and bindings the Linux VDA needs, backing up the original as .prelinux. In Citrix Studio (which had no "Linux OS" concept yet) you created a Machine Catalog choosing Windows Server OS - this implied the shared-desktops model appropriate for Linux; Windows Desktop OS would imply single-user-per-machine, which Linux VDA v1.0 did not support. PVS, MCS and power management were unsupported for Linux VDA v1.0, so you selected "machines that are not power managed" and "another service or technology". The Delivery Group had to be Desktops only (no app delivery yet). Registration could take up to 2 minutes because the controller's endpoints were only updated after the VDA was first configured; the VDA retried on a doubling wait-time algorithm capped at 2 minutes.

*Bron: blogpost '@XDtipster - Linux VDA setup on CentOS 6.6 Pt.3' (2015-07-23), basvankaam.com.*

## Verwante notities

- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [FMA lets one Delivery Group span Catalogs with different OSes (2013 feature)](fma-mixed-os-catalogs-one-delivery-group.md)
- [FMA Power Management as a niche, not-for-everyone capability](fma-power-management-niche-feature.md)
- [FMA Server VDA vs Desktop VDA: multi-session and direct controller comms](fma-server-vda-vs-desktop-vda.md)
- [Host Connection key takeaways: MCS/PVS and cloud support](host-connection-mcs-pvs-cloud-support-key-takeaways.md)
- [Using CentOS 6.6 to test the Citrix Linux VDA (unsupported but code-close to RHEL)](linux-vda-centos-unsupported-but-usable-for-testing.md)
- [Linux VDA install dependencies and ctxsetup.sh configuration](linux-vda-install-config-dependencies.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [Everything you do in Studio is PowerShell underneath](studio-is-powershell-underneath.md)
- [VDA registration and how to verify it](vda-registration-and-verification.md)
