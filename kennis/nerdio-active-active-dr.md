---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, disaster-recovery, fslogix, resilience]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Active/Active DR for AVD Across Two Regions

Nerdio provides almost fully automated active/active DR: machines and user profiles are spread across two separate regions so that an issue in one region does not take out all capacity. Lower blast radius rather than a hard 100% guarantee.

Related standby pattern Bas describes: a second Nerdio installation configured in standby in a different region, ready to spin up a spare set of machines if a disaster hits. The spare can be reserved capacity or pay-per-use; pay-per-use carries no availability guarantee and you may be competing for the same compute when everyone else is failing over too.

Security context Bas always states: Nerdio installs into the customer's own tenant (it is not a managed application), so it is shielded from the outside and all Microsoft security best practices apply to it. Machines deployed through Nerdio can be auto-configured with current Microsoft security features: always prompt for password, encryption at host, boot diagnostics, watermarking, trusted launch, secure boot, vTPM.

See also: nerdio-cost-optimization-levers.

*Bron: Nerdio-content 'MCS' ((root)).*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [AVD / Windows 365 Discovery Questions (Bas's Talking Points)](avd-w365-discovery-questions.md)
- [Bas on disaster recovery: no blueprint, and don't forget the BUDGET](bas-on-disaster-recovery-and-budget.md)
- [DR/HA Discovery Questions for AVD and Nerdio](dr-ha-discovery-questions-avd.md)
- [Nerdio AVD resilience and DR features](nerdio-avd-resilience-features.md)
- [Azure API limits and Nerdio's API Limit Booster](nerdio-azure-api-limit-booster.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [Resilience is about identity, not the device](resilience-is-identity-not-device.md)
- [Windows 365 Reserve (Cloud PC panic button)](windows-365-reserve-explainer.md)
- [Disaster recovery for WVD: keep machines off until needed](wvd-disaster-recovery-cost-angle.md)
