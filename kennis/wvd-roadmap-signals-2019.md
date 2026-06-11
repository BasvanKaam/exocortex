---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, roadmap, msix-app-attach, citrix-daas]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD roadmap signals from the 2019 workshop

Forward-looking items Microsoft shared at the May 2019 workshop (how the future was being signposted then):

- A new Azure WVD management portal was coming; most manual PowerShell/scheduled-task steps (scaling script, image updates, hostpool/desktop/app assignment) would be automated there. Existing PowerShell cmdlets would stay; new ones would be added.
- Azure-AD-exclusive auth (no sync with on-prem AD) and Azure AD security groups for assignment were 'coming'.
- MSIX App Attach, a new native form of app layering, would become the native app-management method for WVD (Microsoft moving away from App-V), but ~a year out.
- Citrix would offer Citrix DaaS using the Windows multi-user WVD image; partner status and a mandatory certification required, but no strict revenue obligations.
- Multi-tenancy via Azure AD B2B was not yet possible but planned.
- Microsoft was investigating Azure Stack for on-prem WVD; general on-prem WVD seemed out of the question. At that point it was no longer technically possible to connect WVD to on-premises.
- WVD Win10 multi-user images would follow the same lifecycle, update channels and build numbers as Windows 10.
- WVD APIs were not allowed yet; that would change at GA, another partner value-add.

*Bron: blogpost '49 facts listed - What I picked up during a WVD Solution Design Workshop' (2019-05-13), basvankaam.com.*

## Verwante notities

- [Citrix Managed Desktop: single-bill DaaS on Citrix-managed Azure](citrix-managed-desktop-model-2019.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
- [App attach is rebranded layering, but Microsoft's marketing will make it win](msix-app-attach-marketing-will-make-it-popular.md)
- [Framing WVD rollout as phases, mapping partners onto each step](wvd-adoption-as-phases-with-partners.md)
- [WVD Fall vs Spring release (non-ARM vs ARM)](wvd-fall-vs-spring-release.md)
- [WVD hit general availability on September 30, 2019](wvd-ga-date-sept-2019.md)
- [WVD is not a near-term threat to Citrix; enterprise features still favor CTX](wvd-not-a-near-term-threat-to-citrix.md)
- [On-prem WVD looks off the table, GA by summer 2019](wvd-on-prem-out-of-question-positie.md)
- [Not WVD on-prem, but a pragmatic middle ground](wvd-on-prem-workarounds-positie.md)
- [WVD preview constraints (2019)](wvd-preview-good-to-knows.md)
- [WVD tenant setup gotchas (2019 workshop)](wvd-tenant-setup-gotchas-2019.md)
- [WVD will evolve quickly because it's cloud-native](wvd-will-evolve-quickly-positie.md)
