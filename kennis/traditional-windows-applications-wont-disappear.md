---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [windows-applications, legacy, saas, hybrid, iaas]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Why traditional Windows applications won't disappear

A central pillar of Bas's paper: a SaaS-only world (browser suffices, no backend, IT only thinks about data) is far away. Windows applications, branded "legacy" by many (Bas prefers "traditional"), will persist for decades. They'll shrink in number, but very slowly.

His figures (Fortin, 2018): Windows 10 already serves 35 million application titles, 175+ application versions, and 16 million unique hardware/driver combinations. SaaS sells like hot bread, yet new traditional Windows apps still arrive daily.

An average relatively small European organisation already runs hundreds of Windows apps, many of them outdated yet indispensable to core business. Not every Windows app gets a SaaS counterpart — the answer is no. Even at an (ambitious) pace of two to three migrations per month, it would take years, in most cases decades.

Moving traditional Windows apps to IaaS rarely gives the desired result either: latency sensitivity matters, and these apps usually depend on other systems (database, shared storage, web server, load balancer) that often can't or may not move along. They usually can't use cloud-native services (direct Blob/S3 storage integration, auto-scaling), so many normal cloud advantages don't apply.

The "doesn't apply to start-ups" objection: true for a real start-up, but not always a new company — e.g. a franchise has its apps decided for it, and a parent company or large investor usually means "use what's already there." So the Windows-app ecosystem persists for years, on-premises is far from extinct, and hybrid is the only possible way forward.

## Bron-citaten (NL, verbatim)

> “After a nuclear war, it'll be cockroaches and Windows apps” – Shawn Bass, CTO End User Computing, VMWare (Bass, 2017)
>
> legacy (traditioneel heeft de voorkeur)

## Verwante notities

- [Bas's list of reasons companies stay (partly) on-premises](bas-objections-to-full-cloud-migration.md)
- [Bas: only ~50-60% of apps can be virtualised](bas-on-virtualisation-coverage-50-60-percent.md)
- [Bas's paper: Cloud Only? No. Cloud First or Hybrid? Yes.](bas-paper-cloud-only-no-cloud-first-yes.md)
- [Paper conclusion: Cloud only? Maybe never](bas-paper-conclusion-cloud-only-never.md)
- [Bas's reframe: call them 'traditional' applications, not 'Legacy'](bas-traditional-not-legacy-applications.md)
- [Bas's warning: Cloud apps with on-premises backends invite latency trouble](latency-cloud-app-onprem-backend.md)
- [Why the page file matters in Terminal Server](terminal-server-page-file-copy-on-write.md)
- [Why traditional Windows apps keep hybrid alive for decades](why-windows-apps-keep-hybrid-alive.md)
- [Survey figures on Windows-app persistence (2019)](windows-app-survey-figures-2019.md)
