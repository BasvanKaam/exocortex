---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, positie, high-availability, architecture, cost]
bron: nerdio-blog
---

# Don't make the management tool highly available, spend the budget on compute and storage

Bas's pragmatic HA stance: technically you can make Nerdio Manager for WVD itself highly available, but he advises against it for most deployments. Spend that budget on compute and storage instead.

His reasoning rests on a key architectural property: NMW integrates directly with WVD and native Azure solutions in a non-disruptive way. If NMW breaks or needs reinstalling, the running environment keeps working, sessions still broker, data stays accessible. Recovery numbers he cites: a fresh NMW setup takes ~45 minutes, onboarding an existing WVD environment ~15-20 minutes, so full recovery (including re-associating the existing environment) is ~1.5 hours. A good RTO without paying to make the management layer redundant.

The broader point: spend HA budget where the risk actually lives (your VMs and data), not on the orchestration tool that the environment can survive without.

*Bron: Nerdio-content 'Making your 1000+ user WVD deployment highly available!' (Blogs).*

## Verwante notities

- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [AVD / NME outbound firewall allow-list](avd-nme-outbound-firewall-allowlist.md)
- [Don't Spend Budget Making the AVD Management Tool Highly Available](dont-make-the-avd-management-plane-highly-available.md)
- [Nerdio AVD resilience and DR features](nerdio-avd-resilience-features.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [Disaster recovery for WVD: keep machines off until needed](wvd-disaster-recovery-cost-angle.md)
