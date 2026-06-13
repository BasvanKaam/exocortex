---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, disaster-recovery, fslogix, business-continuity, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Nerdio AVD resilience and DR features

Bas's framing of how Nerdio Manager reduces organizational risk and makes AVD resilient. DR/replication is often neglected because it is tricky and costly and needs specific know-how; Nerdio reduces it to filling a few fields and picking dropdown options once region connectivity exists.

Key capabilities described:

- **Active/Active host pool disaster recovery** — distributes session-host VMs across two Azure regions, spreads users across both as they log in, and replicates FSLogix profiles. On a regional failure users keep working in the surviving region.
- **Desktop image backup and geographic replication** — automatic image backups, geo-replicated across regions via integration with Azure Compute Gallery to keep images in sync.
- **FSLogix Cloud Cache support** — Nerdio auto-enables and configures Cloud Cache on DR-enabled host pools; profiles replicate asynchronously across storage locations and fail over automatically if one becomes unavailable.
- **Auto-healing** — automatically detects and repairs broken session hosts so users can connect.

Note: feature availability and timelines are point-in-time (e.g. MSP active/active DR was slated for an early-2022 release); verify current state against live Nerdio docs before stating.

*Bron: Nerdio-content 'White paper cost savings (Nine Ways to Reduce Cost and Risk of DaaS with Nerdio Manager for Enterprise)' (Blogs).*

## Verwante notities

- [Cost savings are the cherry on top; business value and continuity matter more](cost-savings-are-the-cherry-on-top.md)
- [Don't make the management tool highly available, spend the budget on compute and storage](dont-make-nerdio-manager-highly-available.md)
- [Don't Spend Budget Making the AVD Management Tool Highly Available](dont-make-the-avd-management-plane-highly-available.md)
- [DR/HA Discovery Questions for AVD and Nerdio](dr-ha-discovery-questions-avd.md)
- [Active/Active DR for AVD Across Two Regions](nerdio-active-active-dr.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [Windows 365 Reserve (Cloud PC panic button)](windows-365-reserve-explainer.md)
- [Disaster recovery for WVD: keep machines off until needed](wvd-disaster-recovery-cost-angle.md)
