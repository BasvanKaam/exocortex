---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, printing, xenapp, xendesktop, universal-print-server, workspace-app]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix printing barely changed across 2018 releases

A release-by-release record Bas compiled (Jan 2019): across XenApp/XenDesktop 7.16, 7.17, 7.18 and Citrix Virtual Apps and Desktops 1808/1811, native printing saw almost no architectural or feature change, mostly 'various fixes of older print issues'. Concrete changes worth noting: 7.16 let you opt out of installing the Universal Print Server PDF driver via a checkbox or the installer flag /exclude "Citrix PDF Printer Driver"; from 7.17 onward the PDF driver is always installed automatically and older versions are replaced on upgrade; CVAD 1808 and Workspace app 1812 added PDF printing support for Windows (enabled via Studio). Contrast: 2016-2017 had had relatively big printing enhancements.

*Bron: blogpost 'What happened with Citrix Printing throughout 2018?!' (2019-01-08), basvankaam.com.*

## Verwante notities

- [Citrix printing troubleshooting and verification tools](citrix-printing-troubleshooting-tools.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
- [Most Citrix printing pain is still bad drivers and bad architecture](positie-citrix-printing-still-driver-and-design-problem.md)
- [Printing is the perennial pain admins shouldn't have to focus on](printing-is-a-perennial-euc-pain.md)
- [Printing is still critical; Citrix deprioritized it for cloud](printing-still-critical-citrix-deprioritized-it.md)
- [Driverless printing in Citrix/VDI: ScrewDrivers and Simplify Printing](tricerat-screwdrivers-driverless-printing.md)
