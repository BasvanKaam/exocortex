---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [hybrid, latency, region, design, war-story]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Hybrid Latency and the Region-Choice Pitfall

Bas shares a hard-won design lesson. In a hybrid model, the design of the environment has big performance impact. Internet is everywhere and users can connect from almost any device/location, but the connection from your chosen cloud environment to a local datacenter is another story.

If you split systems — e.g. publishing a web portal in your cloud (desktop) environment while the associated databases stay in your own datacenter — you can get latency problems and slow processing/retrieval of information. Your choice of cloud region can play a role here, something Bas says he has unfortunately encountered more than once in practice. His maxim applies: 'goedkoop is duurkoop' (cheap turns out expensive), since cloud service costs differ per region. Usually a design decision or a budget decision lies at the root of it.

## Verwante notities

- [Bas on cost management: cost vs. value and ROI/TCO](bas-on-cost-management-roi-tco.md)
- [Physical and performance limits of working from the cloud](cloud-physical-and-performance-limits.md)
- [Printing and scanning are the trap when hosting RDSH/VDI in the cloud](cloud-printing-scanning-bandwidth-latency.md)
- [A simple DIY method to compare Cloud datacenter latency](diy-cloud-latency-ping-test-method.md)
- [Global cloud scale: regions, zones, and which continent has no datacenters](global-scale-regions-zones-datacenters.md)
- [Hybrid cloud: best of both worlds via ExpressRoute and low latency](hybrid-cloud-best-of-both-worlds.md)
- [Bas's warning: Cloud apps with on-premises backends invite latency trouble](latency-cloud-app-onprem-backend.md)
- [Physical and software performance limits of the cloud](physical-and-software-cloud-performance-limits.md)
- [When the Cloud is a good solution - and when it is not](when-cloud-is-and-isnt-a-good-fit.md)
