---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [positie, disaster-recovery, avd, nerdio]
bron: nerdio-content
---

# DR Is About Apps and Data, Not Fancy Infrastructure

Bas's stance: most clients reflexively ask "what about HA/DR?" without understanding what it actually means, what it takes to get there, or what it costs. A second Nerdio install, replicated images, and duplicated profiles are pointless if the apps and data themselves are not also split, duplicated, or replicated across regions. The infrastructure is the easy part and the wrong thing to obsess over.

He is also blunt about the economics: DR/HA is often a deal breaker once clients realize the budget and the additional operational work involved, and "all of a sudden it becomes less relevant" until disaster actually strikes. Budget is the real constraint for roughly 90% of the European companies he deals with. His pragmatic recommendation: a second NME install in another region is a lightweight, sensible starting point, but only after the basics (a BCP, requirements, prioritized critical apps) exist.

*Bron: Nerdio-content 'CORE DOC... Disaster Recovery and HA for Nerdio and AVD' (Core Docs).*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [Bas on disaster recovery: no blueprint, and don't forget the BUDGET](bas-on-disaster-recovery-and-budget.md)
- [Design for Restore, Not Backup (RPO/RTO/MTPD First)](design-for-restore-not-backup.md)
- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [Don't make the management tool highly available, spend the budget on compute and storage](dont-make-nerdio-manager-highly-available.md)
- [Don't Spend Budget Making the AVD Management Tool Highly Available](dont-make-the-avd-management-plane-highly-available.md)
- [DR/HA Discovery Questions for AVD and Nerdio](dr-ha-discovery-questions-avd.md)
- [Active/Active DR for AVD Across Two Regions](nerdio-active-active-dr.md)
- [Nerdio AVD resilience and DR features](nerdio-avd-resilience-features.md)
- [Disaster recovery for WVD: keep machines off until needed](wvd-disaster-recovery-cost-angle.md)
