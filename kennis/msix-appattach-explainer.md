---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [msix, appattach, app-delivery, fslogix, avd, explainer]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# MSIX AppAttach: what it is and why it matters

Bas's framing of MSIX AppAttach as the future direction of Windows application packaging and delivery on virtual desktops (written 2021, Windows 10 2004-era).

- AppAttach evolved from MSIX, which Microsoft introduced at Build 2018. MSIX is positioned as the modern replacement for the MSI format. It was rumored to eventually replace App-V, though Bas's stance: App-V is still very popular and will be for years to come, Microsoft is only slowly moving away from it. Not an overnight switch.
- AppAttach is natively supported in Windows 10 2004 and up (single- and multi-user). Existing Windows OS APIs perform the actual attach at logon.
- Mechanism: applications get packaged onto a VHD(X) virtual hard disk (just a file, treated like any other by the OS). App-V packages, MSIs and EXEs can be converted into AppAttach containers. The VHD(X) is attached to the OS on demand, creating an abstraction layer / container around the app.
- Key operational benefit: packages are copyable and editable like any file. You update the package out of hours while users keep using the old one, then swap the file and users notice nothing. No need to touch or rebuild the golden image; ongoing app management happens on the fly.
- Pairs naturally with FSLogix Profile Containers, which use the same VHD(X)-attach concept for user profile data. FSLogix technology actually underpins part of the AppAttach solution. When both apps and profile data are separated from the underlying OS, you get high flexibility.
- Bas's claim at the time: AppAttach is the #1 preferred approach for app delivery on WVD; FSLogix is the #1 preferred approach for profile management on WVD.

*Bron: Nerdio-content 'Introducing, Microsoft's MSIX AppAttach is now part of Nerdio Manager for WVD' (Blogs).*

## Verwante notities

- [App-V is not dead yet, despite MSIX](app-v-not-dead-yet.md)
- [Application layering toward a zero-app golden image](application-layering-zero-apps-in-golden-image.md)
- [AVD Application Management Strategy with Nerdio](avd-application-management-strategy-nerdio.md)
- [A six-pillar application management strategy for AVD](avd-application-management-strategy-six-pillars.md)
- [FlexApp One application layering, and how it compares to MSIX](flexapp-one-application-layering-explained.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
- [Setting up MSIX App Attach v2 in Nerdio and publishing apps](msix-appattach-v2-publish-nerdio.md)
- [MSIX positioned to replace App-V (2019 transition)](msix-replacing-app-v.md)
