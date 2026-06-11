---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, app-v, vda, studio, automation]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XD7 auto-discovers installed apps; App-V replaces Citrix profiling

How it worked in XenDesktop 7. During application creation the Delivery Controller queries the powered-on machine through the Virtual Agent (VDA) for installed applications and lists them in Studio, and also queries any connected App-V servers. You just tick the apps you want, no one-by-one publishing and no manual double-checking of session-sharing settings (you can still add apps manually by browsing the system). Citrix claimed the simplified workflows and automated configuration checking eliminate up to 80% of deployment time and effort.

Citrix application *profiling* (streaming) is no longer supported in XD7. App-V is integrated instead as the application-virtualization path.

*Bron: blogpost 'How to: Application creation in XenDesktop 7' (2013-07-10), basvankaam.com.*

## Verwante notities

- [Limited AppDNA in XD7 is still a smart inclusion](appdna-in-xd7-limited-but-good-direction.md)
- [Intelligent Configuration Validation and built-in Profile Management](excalibur-built-in-config-validation.md)
- [Excalibur drops Citrix Profiling (app streaming) for App-V (2013 Synergy news)](excalibur-drops-profiling-for-appv.md)
- [Microsoft App-V components and licensing with Citrix](microsoft-app-v-with-citrix.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
- [Everything you do in Studio is PowerShell underneath](studio-is-powershell-underneath.md)
- [XD7 app creation: Catalog then Delivery Group then App](xd7-catalog-delivery-group-app-flow.md)
