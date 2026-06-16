---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, azure, projectmanagement, adoptie, application]
layer: reference
gedateerd: nee
bron: nerdio-blog
---

# AVD/Azure project readiness framework

Bas's five non-technical things to settle before starting an AVD/Azure migration. These are about people and process, not Azure resources.

1. **Responsibilities and the right resources** — clearly assign who builds, who documents, who tests applications, who educates/escorts users. One person can own multiple roles; what matters is that ownership is explicit and that people have time actually reserved for the work. Unallocated time is the main reason projects run long: 'fires' shift priorities, so set a baseline everyone can fall back to.
2. **Goals and success criteria** — define up front what success looks like and how it is measured (desired results, automated critical features working as expected, costs in line with projection). Without a measurable definition there is no point. This is the basis for reviewing outcomes at the end of a trial or project window.
3. **Applications** — application compatibility is the most common migration challenge. Inventory the number and types of apps to estimate testing effort. Use the Retain / Refactor / Rehost / Repurchase / Retire framing to decide what to drop or move to SaaS. Apps may need more (sometimes less) compute on a cloud VM; transitions are rarely one-to-one. Decide delivery (RemoteApp vs published desktop, icons vs start menu vs client) and ongoing image-management strategy.
4. **Data** — keep data as close to the hosts and users as possible to limit latency. Understand how much data there is and what it's used for to prioritize migration order. Migration is tricky because live data always has a delta to replicate; find the moment to cut over and disable the old environment. Consider archiving to clean up first.
5. **Educating and involving users** — the single biggest adoption factor. Involve users early, ask for their input, explain the why (legacy retirement, future-proofing, security) and what's in it for them. Late, big-bang rollouts ('BANG, here you go') produce low adoption.

Cross-cutting checks for apps and data: legal/compliance restrictions on running in public cloud, dependencies (e.g. legacy dongles, linked systems), encryption/authentication needs, and networking/latency/IO requirements (cloud differs from on-prem).

There is no single golden approach; tailor per company.

*Bron: Nerdio-content 'Top 5 things to consider before starting your AVD / Azure journey' (Blogs).*

## Verwante notities

- [Moving 32-bit to 64-bit (and 2003 to 2008) means app-compat work (durable lesson)](32bit-to-64bit-app-compat-is-a-fact-of-life.md)
- [Ambassadors and skill readiness in the execution phase](ambassadors-skill-readiness.md)
- [AVD / Windows 365 Discovery Questions (Bas's Talking Points)](avd-w365-discovery-questions.md)
- [Bas: The 6 R's for Application Rationalization](bas-6-rs-cloud-migration.md)
- [Common WVD/Azure adoption challenges (from the field)](common-wvd-adoption-challenges.md)
- [Criteria for Selecting the First Workload to Migrate](first-workload-selection-criteria.md)
