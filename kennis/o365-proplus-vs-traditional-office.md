---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [office-365, microsoft, licensing, whitepaper]
layer: reference
gedateerd: ja
bron: salomon-whitepaper
---

# Office 365 ProPlus versus traditional Office

From Bas van Kaam's 2019 whitepaper. The core distinction he draws:

- Traditional Office (2010/2013/2016/2019) is a one-off purchase (Capex); ProPlus is a subscription (Opex). 365 billed monthly, ProPlus yearly.
- ProPlus continuously receives the latest features plus security updates (weekly/monthly) via the Azure cloud. Office 2019 only gets security updates, no new features. To move to a newer Office version you must repurchase.
- Both use the Click-to-Run install method; from Office 2019 onward Click-to-Run is the only available method, including for traditional Office.
- ProPlus tracks the Windows 10 Semi-Annual Channel release; Office 2019 tracks the Long Term Servicing Channel (e.g. Windows 10 / Server 2019). This is why the feature gap is large.
- Activation: ProPlus activates online per user; Office 2019 uses KMS or MAK. ProPlus needs internet only for a license check every 30 days, not continuously.
- ProPlus is NOT the online (browser) version: that is Office Online. ProPlus and traditional Office cannot run side by side.
- ProPlus works alongside existing on-premises Exchange and SharePoint, and is managed with the same tools as traditional Office (SCCM, Group Policy).

Time-bound: written against the 2019 Office/365 landscape; product names and channel mechanics have since changed.

*Bron: Salomon-IT 'Whitepaper'.*

## Verwante notities

- [Office 365 ProPlus on Remote Desktop Services](o365-proplus-on-rds.md)
- [Controlling ProPlus diagnostic data and connected services](o365-proplus-privacy-controls.md)
- [Office 365 ProPlus Update Channels model](o365-update-channels-model.md)
- [Office 365 ProPlus versus traditional Office](office-365-proplus-vs-traditional-office.md)
- [Office vs Office 365 vs Office 365 ProPlus: what is what](office-vs-office365-vs-proplus.md)
- [ProPlus is usually the better choice over traditional Office](position-proplus-preferred-over-traditional-office.md)
