---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, nerdio, disaster-recovery, high-availability, method, discovery]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# DR/HA Discovery Questions for AVD and Nerdio

Before designing any DR/HA setup, Bas starts from requirements, not technology. His opening questions:

- **RTO (Recovery Time Objective)**: how fast do you need to be back up at a minimum?
- **RPO (Recovery Point Objective)**: how much data are you willing to lose?
- Is there a **Business Continuity Plan** at all (prevention and recovery for natural disaster, cyber-attack)?
- What is the **budget**? Multiple instances of NME cost extra, and a failover site sitting in a shutdown state still costs.
- Which **critical workloads/apps** exist? Prioritize them and account for their replication, databases, storage accounts.

If none of this exists yet, start there before spending time and money on redundancy. That groundwork is the first deliverable.

## What is actually worth making redundant

Not every component is critical to back up or duplicate:

- Use the **Azure Compute Gallery** so images are redundant; you can spin up a fresh AVD environment (with business-critical apps baked into the image) even without Nerdio.
- User profiles (FSLogix) are not critical per se. Cloud Cache is optional here; not worth heavy investment.
- Keep a **secondary NME install in another region on standby**, including images. In an emergency, turn on autoscale and users can log back in fairly quickly. This is lightweight and a good first step.

## The core principle

If an Azure region goes down and all your data and apps live in that region, a second NME install and replicated images do not save you. The data and apps must be split / duplicated / replicated too. It is not just the infrastructure. In the end it is all about the apps and data; a fancy double or triple AVD/Nerdio infrastructure does you no good if you cannot reach your apps and their associated data (databases, storage accounts).

## References
- Nerdio BCDR guidance KB (nmw.zendesk.com)
- Microsoft disaster-recovery overview and the AVD-specific DR doc on Microsoft Learn

*Bron: Nerdio-content 'CORE DOC... Disaster Recovery and HA for Nerdio and AVD' (Core Docs).*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [AVD / Windows 365 Discovery Questions (Bas's Talking Points)](avd-w365-discovery-questions.md)
- [Bas on disaster recovery: no blueprint, and don't forget the BUDGET](bas-on-disaster-recovery-and-budget.md)
- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [Don't Spend Budget Making the AVD Management Tool Highly Available](dont-make-the-avd-management-plane-highly-available.md)
- [Active/Active DR for AVD Across Two Regions](nerdio-active-active-dr.md)
- [Nerdio AVD resilience and DR features](nerdio-avd-resilience-features.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [Resilience is about identity, not the device](resilience-is-identity-not-device.md)
- [Vertical-tailored discovery deck for smaller opportunities](vertical-discovery-deck-method.md)
- [Windows 365 Reserve (Cloud PC panic button)](windows-365-reserve-explainer.md)
- [Disaster recovery for WVD: keep machines off until needed](wvd-disaster-recovery-cost-angle.md)
