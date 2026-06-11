---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenapp, xendesktop, platinum, licensing, editions, netscaler]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# What XenApp/XenDesktop Platinum added over Enterprise

How the Platinum edition stacked up in late 2016 (roughly ~1/3 more than Enterprise for XenApp). Thirteen Platinum-tier features/services he catalogued:

- HDX seamless applications (blend locally installed apps into the virtual desktop; tech first introduced and patented by RES).
- SD-WAN plug-in (software accelerator, part of NetScaler SD-WAN, formerly CloudBridge).
- StoreFront Self Service Password reset (users reset/unlock their own accounts, saves helpdesk calls).
- Workspace Environment Manager (formerly Norskale, recently acquired; note: also available to Enterprise). Complements Citrix User Profile Management.
- Common Criteria certification (security cert used by 25+ countries).
- Smart Access (context-based policy via NetScaler Gateway to grant/deny printing, copy/paste, drive mapping, etc.).
- SCOM Management Packs (formerly Comtrade, acquired Jan 2016; 9 packs for XenServer, StoreFront, NetScaler, License Server, PVS, etc.; integrate alerts into Director). Frequently criticized as too expensive.
- SSL VPN (via NetScaler, separate Platinum-licensed appliance).
- Session Recording / Smart Auditor (time-stamped visual session recording for compliance/security/support).
- Director Platinum (up to a year of historical data, SCOM alerts, OS usage reporting, proactive alerting, Octoblu and NetScaler MAS integration).
- User Experience network analysis (NetScaler HDX Insight in Director).
- AppDNA incl. App Disks (discover/model/manage apps for migration; App Disks are in all editions, AppDNA is not).
- Provisioning Services (PVS) for server workloads (XenApp-only customers need Platinum; XenApp-as-part-of-XenDesktop needs only Enterprise).
- Microsoft System Center integration (Citrix Connector for SCCM).

Note: many of these require a separately purchased, Platinum-licensed NetScaler.

*Bron: blogpost 'What the Citrix XenApp/XenDesktop Platinum edition actually gives you' (2016-11-28), basvankaam.com.*

## Verwante notities

- [Citrix license type vs edition vs consumption model](citrix-license-type-vs-edition.md)
- [Platinum grows in worth, but unbundle the editions](platinum-worth-it-and-unbundle-editions.md)
