---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, windows-10-multi-user, licensing, fslogix, windows-7-esu]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD introduced multi-user Windows 10 and a license-based entitlement model

Key early WVD facts (2019): WVD introduced a new multi-user (Enterprise) Windows 10 OS built on the same RDS technology used in Windows Server, alongside support for Server 2012 R2/2016/2019 and single-user Windows 7/10. The WVD control panel (service) itself is free of charge under qualifying licenses (Microsoft 365 E3/E5/A3/A5/Business or Windows E3/E5/A3/A5; server OS needs an RDS CAL with Software Assurance); you pay only for the Azure IaaS resources consumed. Windows 7 on WVD got extended security updates (ESU) free until 2023 on Azure. FSLogix handles profile containers and adds Outlook/Windows search caching, OneDrive files-on-demand, Teams support, Cloud Cache with storage failover, and Application Masking. Win10 single and multi-user are Semi-Annual Channel; Server 2012 R2/2016/2019 are LTSC. Load balancing for Win10 multi-user came in Breadth (default, even spread, reserved instances) and Depth (fill one VM to a configurable user count before spinning up the next).

How it worked then; licensing and channel specifics are dated, but the multi-user Windows 10 + per-user license entitlement model became the foundation of Azure Virtual Desktop.

*Bron: blogpost 'The Windows Virtual Desktop - what we know so far. 83 facts listed' (2019-03-19), basvankaam.com.*

## Verwante notities

- [M365 E3 already entitles you to AHU for WVD](ahu-entitlement-via-m365-e3.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Microsoft VDA vs RDS licensing for Citrix](microsoft-vda-rds-licensing-for-citrix.md)
- [Prediction: a multi-user version of Windows 10 is coming](prediction-multi-session-windows-10.md)
- [How Windows 10 multi-session came to light (2018)](windows-10-multi-session-origins-2018.md)
- [WVD session hosts are charged at Linux compute rates](wvd-charged-at-linux-rates.md)
- [Windows 10 Enterprise multi-session performance debate (Ignite 2019)](wvd-ignite-2019-multisession.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
- [WVD Whitepaper: The Selling Points](wvd-whitepaper-propositions.md)
