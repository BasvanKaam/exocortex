---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, disaster-recovery, rto, positie]
bron: nerdio-blog
---

# Don't Spend Budget Making the AVD Management Tool Highly Available

Bas's stance: making Nerdio Manager itself highly available is technically possible but he advises against it for most cases. Spend that budget on compute and storage instead.

His reasoning rests on a non-disruptive integration argument: because Nerdio integrates directly with WVD/AVD and native Azure services, sessions keep being brokered and data stays accessible even if the management installation breaks. Recovery is fast enough that HA on the management layer isn't worth the spend: associating an existing WVD environment back is ~1.5 hours, a fresh Nerdio Manager setup ~45 minutes, and onboarding an existing environment ~15-20 minutes depending on machine count. "Not a bad RTO."

The broader position: a real DR plan is more than Availability Sets/Zones plus redundant storage; those are the low-hanging fruit, not the destination.

*Bron: Nerdio-content 'Making your WVD deployment highly available' (Blogs).*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [Don't make the management tool highly available, spend the budget on compute and storage](dont-make-nerdio-manager-highly-available.md)
- [DR/HA Discovery Questions for AVD and Nerdio](dr-ha-discovery-questions-avd.md)
- [Nerdio AVD resilience and DR features](nerdio-avd-resilience-features.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [Disaster recovery for WVD: keep machines off until needed](wvd-disaster-recovery-cost-angle.md)
