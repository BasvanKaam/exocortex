---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, ltsr, current-release, servicing, lifecycle]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix LTSR vs CR servicing model

How it worked in 2016, when Citrix introduced two XenApp/XenDesktop servicing options at Summit 2016.

**LTSR (Long Term Service Release):** built for stability and supportability. Gives 5 years mainstream support plus an optional 5 years extended support (purchased separately, ~6 months before mainstream ends). Receives cumulative updates every 4 to 6 months (these replaced the old Hotfix Rollup Packs), and a new LTSR version of XenApp/XenDesktop roughly every 12 to 24 months. Crucially: no new functionality is added during an LTSR lifecycle, only fixes. That feature freeze is exactly why Citrix can near-guarantee a stable product. Requires a valid Software Maintenance (SM) contract; without SM you cannot download cumulative updates. 7.6 was the first-ever LTSR, preceded by three Feature Packs.

**CR (Current Release):** access to the newest versions and all the latest features, on shorter cycles (a new version every 3 to 9 months in general). Full product updates impacting Delivery Controllers, VDAs, StoreFront, etc. Requires at least a valid Subscription Advantage contract. The CR was not actually new, it was just a name for the standard release process as it had always been, created so Citrix could better distinguish the two and keep the spotlight on the LTSR.

Key nuances: you can run LTSR and CR side by side; switching either direction is optional; upgrading to a newer LTSR resets the 5-year clock so you are never truly stuck on one version for 5 years; Citrix does not recommend mixing non-compliant CR components (e.g. PVS, StoreFront) into an LTSR environment, though it is supported.

*Bron: blogpost 'The Citrix Long Term Service Release vs. the Current Release. What's (really) new?' (2016-04-06), basvankaam.com.*

## Verwante notities

- [Bas's take: the Current Release isn't really new](bas-current-release-not-really-new.md)
- [Citrix support model shift to Customer Success Services](citrix-customer-success-services-2017.md)
- [Citrix editions, Subscription Advantage and Software Maintenance](citrix-editions-subscription-advantage-software-maintenance.md)
- [Citrix LTSR vs Current Release](citrix-ltsr-vs-current-release.md)
- [The rapid Current Release cadence makes sense](defence-of-citrix-rapid-release-cycle.md)
- [LTSR is the right call, but not for everybody](ltsr-is-not-for-everybody.md)
- [Windows Server 2019 at announcement: LTSC/SAC, RDSH question, RDmi](windows-server-2019-ltsc-sac-rdmi.md)
- [Windows 10 servicing branches and deployment rings](windows10-servicing-branches-rings.md)
- [XenApp/XenDesktop 7.12 new features and the CR/LTSR model](xenapp-712-whats-new.md)
