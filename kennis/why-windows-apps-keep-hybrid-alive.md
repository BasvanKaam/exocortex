---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [hybrid, windows-apps, legacy, iaas, saas, euc]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Why traditional Windows apps keep hybrid alive for decades

Bas's argument (2019, still largely holds) for why a SaaS-only world stays out of reach:

- Windows apps (he prefers 'traditional' over 'legacy') will be around for decades; their numbers decline only painfully slowly. Context figure: Windows 10 supported 35M+ application titles, 175+ versions, 16M+ hardware/driver combinations (Fortin, 2018). New traditional Windows apps are still built daily.
- A typical small/mid European company easily runs hundreds of Windows apps, many aging yet business-critical. Not every Windows app has a SaaS alternative, and even migrating 2-3 per month would take years to decades.
- Rehosting Windows apps in IaaS rarely delivers: latency sensitivity, dependencies on databases/shared storage/web servers/load balancers that often can't all move, and inability to use cloud-native features (no native blob/S3 integration, no platform auto-scaling). Many cloud benefits simply don't apply to these apps.
- The 'startups have no legacy' counter only holds for true startups. Franchises, companies with a parent or major investor, etc. usually inherit a mandated stack, typically traditional Windows apps with some SaaS layered on top. This keeps Windows alive, keeps on-prem relevant, and confirms hybrid as the realistic path.

**Workspace aggregators** reinforce the point: portals aggregate web/mobile/SaaS/Windows apps/desktops/data into one web portal, often with an RDSH backend spinning up server farms on-prem or in cloud to deliver published apps / shared desktops, the same model used for 20+ years. To the user it looks like SaaS while the backend still relies on traditional file/print/app systems. Survey demand for such Unified Workspace Portals was high (70.5% yes in van Kaam & Brinkhoff, 2019).

*Link to: position-cloud-first-not-cloud-only.md, cloud-promises-reality-check.md.*

*Bron: Nerdio-content 'Cloud only No. Cloud First or Hybrid Yes.' (Blogs).*

## Verwante notities

- [What actually slows cloud adoption (and why cloud-first beats cloud-only)](cloud-blockers-and-the-cloud-first-case.md)
- [Physical and performance limits of working from the cloud](cloud-physical-and-performance-limits.md)
- [The cloud's promises, line by line (Bas's reality check)](cloud-promises-reality-check.md)
- [Call them traditional Windows apps, not legacy](positie-windows-apps-traditional-not-legacy.md)
- [Cloud only? No. Cloud first or hybrid? Yes.](position-cloud-first-not-cloud-only.md)
- [Call them traditional Windows apps, not legacy, and AVD keeps them alive](position-traditional-not-legacy-windows-apps.md)
- [Why traditional Windows applications won't disappear](traditional-windows-applications-wont-disappear.md)
- [Workspace aggregators and the Unified Workspace Portal](workspace-aggregators-unified-workspace-portal.md)
