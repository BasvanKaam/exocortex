---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenapp, xendesktop, 7.12, current-release, ltsr, tags, director]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenApp/XenDesktop 7.12 new features and the CR/LTSR model

What 7.12 introduced (December 2016) and how the release model worked:

Release model: Citrix split into Current Release (CR, new features every 3-6 months, then closer to 3) and Long Term Service Release (LTSR, stable, 5 years support extendable to 10, maintained via Cumulative Updates with no new features). 7.6 was the first LTSR. The 7.5 release was mainly notable for XenApp becoming a separate purchase/product again. Cloud-first: features are developed and tested in Citrix Cloud, then flow to on-premises.

7.12 features:
- Local Host Cache (see separate LHC note).
- Machine Tags: tag individual machines within Delivery Groups (apps could already be tagged) so specific machines are considered for launch while others are left alone, letting one set of machines serve multiple purposes and saving cost.
- Per-Delivery-Group restart schedules via PowerShell, including tag-based schedules that restart only tagged machines.
- Citrix Insight Services install/upgrade analytics upload now enabled by default; the GUI toggle is gone (disable only via Registry or a new command-line option).
- CEIP enabled by default on new 7.12 VDA installs.
- Azure Resource Manager enhancements.
- New lightweight VDAWorkstationCoreSetup.exe (Desktop OS VDA for Remote PC Access / VDI; excludes App-V, Profile Management, MIS, Personal vDisk, Receiver).
- Director: friendlier failure descriptions, up to one month historical data in Enterprise, custom reporting, SNMP-trap notifications.
- Session Recording: IP/IP-range policy criteria, idle-period highlighting, TLS 1.2.
- VDA: 8-bit colour depth Thinwire, HTML5 video redirection for internal sites, universal print driver stapling/paper-source in EMF, keyboard layout sync, Framehawk over NetScaler Gateway HA.
- Evaluation-only: new enlightened data transport layer over UDP for long-haul WAN/Internet, improving throughput across ICA virtual channels (later known as EDT).
- StoreFront 3.8: multiple IIS web sites, Firefox client detection/launch.

*Bron: blogpost 'What's new in XenApp & XenDesktop 7.12, and why the rapid release cycle makes sense' (2016-12-06), basvankaam.com.*

## Verwante notities

- [Citrix LTSR vs CR servicing model](citrix-ltsr-vs-cr-servicing.md)
- [The rapid Current Release cadence makes sense](defence-of-citrix-rapid-release-cycle.md)
- [LTSR is the right call, but not for everybody](ltsr-is-not-for-everybody.md)
