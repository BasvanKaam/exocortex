---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, wvd, disaster-recovery, autoscale, entra]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Disaster recovery for WVD: keep machines off until needed

Bas's DR angle for cloud/hybrid virtual desktops, framed around cost-efficient resilience rather than heavy DR tooling:

- DR matters even for 100% cloud-native shops, not only hybrid ones.
- Switch disk types and run machines only when they need to run: stand-by capacity without high standing costs.
- Autoscale builds out the environment for you, so deep Azure knowledge isn't required to stand up a DR target.
- Identity: both Azure AD and traditional AD work. Azure AD is easier because you don't have to worry about computer account passwords resetting every ~30 days, which otherwise blocks machines that have been parked from starting again.
- Keep images in sync across regions via the Shared Image Gallery.

This is a fragment of working notes, so treat as a checklist of his DR talking points.

*Bron: Nerdio-content 'Disaster Recovery with Neil' (Blogs).*

## Verwante notities

- [Don't make the management tool highly available, spend the budget on compute and storage](dont-make-nerdio-manager-highly-available.md)
- [Don't Spend Budget Making the AVD Management Tool Highly Available](dont-make-the-avd-management-plane-highly-available.md)
- [DR/HA Discovery Questions for AVD and Nerdio](dr-ha-discovery-questions-avd.md)
- [Active/Active DR for AVD Across Two Regions](nerdio-active-active-dr.md)
- [Nerdio AVD resilience and DR features](nerdio-avd-resilience-features.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [WVD high availability: what you actually own vs what Microsoft owns](wvd-high-availability-architecture.md)
