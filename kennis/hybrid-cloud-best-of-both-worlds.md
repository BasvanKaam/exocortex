---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [hybrid-cloud, expressroute, daas, latency, on-premises]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Hybrid cloud: best of both worlds via ExpressRoute and low latency

A hybrid cloud combines an organisation's own datacenter (on-premises) with a public cloud (Azure, AWS, Google). Direct connections - ExpressRoute (Azure), Direct Connect (AWS), Interconnect (GCP) - link the owned infrastructure to the cloud so workloads and data can be exchanged between both.

Bas notes he regularly deals with companies that want to keep part on-premises and move a large part to cloud. A common pattern: a DaaS-based cloud environment where almost all users get a virtual desktop plus a set of applications differing per business unit, with an ExpressRoute laid between their datacenter and the Azure cloud. This keeps sensitive data and business-critical apps in their own datacenter for control and security, and an ExpressRoute connection almost always gives much lower latency - important especially for older applications. Hybrid cloud offers the best of both worlds.

## Bron-citaten (NL, verbatim)

> De hybride Cloud biedt bedrijven het beste van beide werelden.

## Verwante notities

- [Bas's list of reasons companies stay (partly) on-premises](bas-objections-to-full-cloud-migration.md)
- [Bas's paper: Cloud Only? No. Cloud First or Hybrid? Yes.](bas-paper-cloud-only-no-cloud-first-yes.md)
- [Bas on the future limits of self-hosting your own data growth](bas-self-hosting-data-growth-limit.md)
- [Cloud deployment models (public, private, hybrid, community)](cloud-deployment-models.md)
- [DaaS versus VDI](daas-vs-vdi.md)
- [Hybrid Latency and the Region-Choice Pitfall](hybrid-latency-region-choice-pitfall.md)
- [Bas on cloud, hybrid and the future of on-premises VDI](is-cloud-vdi-still-relevant-takeaways.md)
- [Bas's warning: Cloud apps with on-premises backends invite latency trouble](latency-cloud-app-onprem-backend.md)
- [Bas's mini business case: the current-vs-possible mapping table](mini-business-case-current-vs-hybrid-table.md)
- [Physical and software performance limits of the cloud](physical-and-software-cloud-performance-limits.md)
