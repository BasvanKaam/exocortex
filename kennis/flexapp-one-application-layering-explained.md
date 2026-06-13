---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [flexapp-one, liquidware, application-layering, msix, app-attach, avd, nerdio]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# FlexApp One application layering, and how it compares to MSIX

Bas's explainer on Liquidware FlexApp One application delivery, from the Nerdio integration announcement. Product-specific, treat as dated.

## What FlexApp One does
- Decouples applications from the underlying OS, simplifying ongoing management while offering portability.
- Takes existing apps and (fully automated) transforms them into a **self-contained package** that can be "attached" to any Windows OS, including multi-session, on demand. Apps are layered on top: nothing is installed or stored in the OS itself, so the **base image stays clean**.
- Supports up to **90% of application types** today, including MSIX, MSI, and EXE. By contrast, layering solutions like MSIX cover around **30%**.

## Update model (no business interruption)
- Because packages are decoupled and micro-isolated, apps can be updated without interrupting day-to-day business.
- Packages can be duplicated/copied: while users still access v1, you update the copy, then simply swap packages. No touching the underlying image. Clean, simple, fast.

## With Nerdio
- Nerdio (NME) can assign FlexApp One apps to any AVD workspace **without agents or additional delivery platforms**.
- Delivering a package to an AVD host takes about a minute; because packages are self-contained and executed locally (nothing installed), they start extremely fast, as if installed on a local hard drive.
- FlexApp One packages are not part of the base image, so on each (re)boot Nerdio reapplies the bits needed to run FlexApp to the AVD host(s).

*Bron: Nerdio-content 'Nerdio to support Liquidware's FlexApp One application delivery and management' (Blogs).*

## Verwante notities

- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [Application layering toward a zero-app golden image](application-layering-zero-apps-in-golden-image.md)
- [AVD Application Management Strategy with Nerdio](avd-application-management-strategy-nerdio.md)
- [A six-pillar application management strategy for AVD](avd-application-management-strategy-six-pillars.md)
- [Liquidware suite: ProfileUnity, FlexApp, Stratusphere UX (2018)](liquidware-profileunity-flexapp-stratusphere.md)
- [MSIX AppAttach: what it is and why it matters](msix-appattach-explainer.md)
- [Setting up MSIX App Attach v2 in Nerdio and publishing apps](msix-appattach-v2-publish-nerdio.md)
- [App layering that keeps the base image clean is the right model for AVD](positie-app-layering-keeps-the-image-clean.md)
