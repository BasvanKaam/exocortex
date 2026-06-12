---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [latency, legacy-apps, architecture, iaas, paas, war-story]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Bas's warning: Cloud apps with on-premises backends invite latency trouble

Bas flags a specific architecture as vaak vragen om problemen (often asking for trouble): applications offered in the Cloud while their backend systems still sit on-premises. The latency caused by the physical separation of the two systems often causes severe delays. The Cloud app may need to regularly hit a database to read or write information; older in-house-developed applications especially suffer because they count on fast low-latency throughput, and without it the app shows requested information on screen very slowly.

It is not always possible to move an outdated application to the Cloud - the database type may not be supported as a Cloud service. That does not mean it is technically impossible, but it costs considerable time and money (including Cloud resources). The database might then have to run on an IaaS virtual machine, often more expensive than a modern Cloud service (typically PaaS) that takes over the role of an old-fashioned database server. Alternatively the app itself could be adapted (costly, needs specialist knowledge) or replaced with a modern variant like SaaS, which brings its own challenges - a different way of working, data that cannot be reused, a strange licensing model, etc. Bas's bottom line: the Cloud is no silver bullet, no solution for everything.

## Verwante notities

- [Bas's reframe: call them 'traditional' applications, not 'Legacy'](bas-traditional-not-legacy-applications.md)
- [Bas: 'Wegwerp IT' and the Lift-and-Shift Caution](bas-wegwerp-it-and-lift-and-shift.md)
- [Cloud delivery models: IaaS, PaaS, SaaS and DaaS](cloud-delivery-models-iaas-paas-saas-daas.md)
- [Hidden decision factors before going cloud](cloud-hidden-decision-factors.md)
- [Edge computing and Edge-nodes](edge-computing.md)
- [Hybrid cloud: best of both worlds via ExpressRoute and low latency](hybrid-cloud-best-of-both-worlds.md)
- [Hybrid Latency and the Region-Choice Pitfall](hybrid-latency-region-choice-pitfall.md)
- [Office 365 Network Performance: Service Front Doors and the Basics](office365-network-performance-basics.md)
- [Physical and software performance limits of the cloud](physical-and-software-cloud-performance-limits.md)
- [Why traditional Windows applications won't disappear](traditional-windows-applications-wont-disappear.md)
