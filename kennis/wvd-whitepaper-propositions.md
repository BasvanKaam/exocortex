---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [wvd, azure, daas, cost, scalability, licensing, covid]
layer: reference
gedateerd: ja
bron: salomon-wvd
---

# WVD Whitepaper: The Selling Points

The argument structure Bas uses to sell WVD to a business audience (COVID-era whitepaper, ~April 2020). WVD usage reportedly grew 300% in the preceding weeks.

Work from anywhere: a virtual Windows 10 experience on virtually any device (laptop, desktop, thin client, tablet) — only a working internet connection required. It stays Windows 10, so no end-user retraining.

Cost efficiency via multi-session: Windows 10 Enterprise Multi-Session shares one Windows 10 instance across multiple users simultaneously (an "industry first"). More with less on the underlying CPU/memory/storage. You can also publish individual apps instead of full desktops, and Windows Server (2012 R2 / 2016 / 2019) works the same way.

Maintenance split: Microsoft runs the gateway, load balancing, database and diagnostics. The IT org/partner only maintains apps, data, entitlements, and keeps security patches up to date. Initial VM provisioning is largely automated.

Scalability: 15, 25, 50 or 150 extra virtual workplaces provisioned in 1-2 hours; turn them off / delete them when no longer needed. Good for temporary capacity shortages, acquisitions, interns, hot stand-by, or forced remote work.

Pay-for-use: the WVD service itself is in most cases free with the right entitlement; you pay only for the VMs, and nothing when they are off. Reserving capacity for 1 or 3 years saves an additional 40-70%; automated shutdown during nights/quiet periods saves more.

Licensing entitlements: Microsoft 365 E3/E5/A3/A5/F1/Business; Windows E3/E5/A3/A5; or RDS CAL with Software Assurance.

Windows 7: WVD lets you keep running Windows 7 with free extended security updates until January 2023, so organizations migrate to Windows 10 at their own pace.

Low-risk adoption: start small alongside what you already have, no big upfront investment, grow from there. Related: wvd-explained-bvk-framing, fslogix-five-capabilities.

*Bron: Salomon-IT 'WVD Whitepaper voor Salomon en Avensus' (WVD).*

## Verwante notities

- [Fast, Good, Cheap: You Can Now Pick All Three](fast-good-cheap-pick-three.md)
- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [IT as a Utility](it-as-a-utility.md)
- [The pandemic compressed VDI/DaaS adoption from months to weeks](pandemic-accelerated-vdi-daas-adoption.md)
- [Windows 7 End of Support and the Windows Virtual Desktop (2019)](windows-7-eol-and-wvd-2019.md)
- [WVD Explained: Bas's Core Story](wvd-explained-bvk-framing.md)
- [WVD introduced multi-user Windows 10 and a license-based entitlement model](wvd-win10-multiuser-and-licensing.md)
