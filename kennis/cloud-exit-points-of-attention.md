---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [cloud-exit, checklist, data-export, migration-tools, encryption, dependencies]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Bas's checklist of points of attention for a cloud exit

Bas offers a self-authored 'points of attention' list for a cloud exit - explicitly admitting it is probably not complete but should give a good starting point. Highlights:
- Rules around cloud-service use differ; services can be stopped or changed without notice - study the available SLAs. Coming from a managed service provider, you may also have agreed SLAs toward your own user organisation(s).
- Not all services remain available after termination; data is retained only briefly.
- Impact can be large: CTO, CIO, CFO review the plan and ultimately the CEO approves it.
- An exit strategy is (or can be) wide-ranging - work in an organised way and break it into smaller steps.
- Prioritise: low-hanging fruit / fewest dependencies first, OR the most critical datasets and applications first.
- Inventory meticulously: numbers, quantities, types of data/apps/systems, roles, services, networks.
- Don't underestimate choosing an alternative platform; take your time. Focus first on data and applications, systems follow later.
- How fast and in what way can you reach your data and machines? In what format can data be exported - this is not fixed. Beyond data format you may face transfer of contracts and licence agreements (licence use is not equal across providers).
- Map dependencies: app-to-app, app-to-infra, data-to-app, system/app-to-network. Can an app or dataset function without the cloud infra?
- Account for data volume/growth and throughput speeds - how long will it take?
- Inventory all possible migration tools (in general and per app/system); know how they work, test them when you don't need them, keep them ready (cloud-to-cloud, cloud-to-on-prem).
- Apply encryption to protect data integrity and security. Watch out for cloud-specific tools and APIs you depend on.
- Consider your own organisation's knowledge level. Can the provider give a guarantee (and proof) that deleted data is actually deleted? And: test, test, test - especially during the preparation phase.

## Bron-citaten (NL, verbatim)

> Testen, testen, testen. Met name gedurende de voorbereidingsfase.
