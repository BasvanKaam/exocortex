---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [msix, app-attach, fslogix, application-layering, wvd, microsoft]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# MSIX app attach: VHD-mounted apps via FSLogix filter drivers

How it worked when it was previewed in 2019. MSIX app attach takes an existing MSIX package, packs it in a VHD, and mounts that VHD onto the OS at user login. FSLogix filter drivers do the work so the OS doesn't know the difference; once attached, the app seems local and behaves as such. The concept is identical to application layering: apps are abstracted so they're easier to manage and update, streamed from a file server, no special deployment servers needed.

Key properties as known then:
- Works virtual and physical, single and multi-user, on-prem and Cloud (Azure, AWS), no OS dependencies and no repackaging of existing MSIX packages.
- Multiple machines can read from a single app attach package simultaneously via block-level, read-only access.
- Assigned per user or per user group, available at login, and works with app masking.
- Packages run in a 'helium container' (unclear at the time how this differs from an App-V container isolation-wise).

Org note: FSLogix sits under the WVD/RDS team, while app attach was developed by the MSIX team within Microsoft.

*Bron: blogpost 'A rundown on what we know about MSIX app attach' (2019-05-15), basvankaam.com.*

## Verwante notities

- [In-guest vs hypervisor-level mounting in application layering](app-layering-in-guest-mounting-explained.md)
- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [How application layering works: filter drivers merging virtual disks](how-application-layering-works-2.md)
- [App attach is rebranded layering, but Microsoft's marketing will make it win](msix-app-attach-marketing-will-make-it-popular.md)
- [MSIX AppAttach: what it is and why it matters](msix-appattach-explainer.md)
- [Setting up MSIX App Attach v2 in Nerdio and publishing apps](msix-appattach-v2-publish-nerdio.md)
- [MSIX positioned to replace App-V (2019 transition)](msix-replacing-app-v.md)
- [Nerdio innovating on top of WVD is 'a perfect marriage'](nerdio-plus-microsoft-perfect-marriage.md)
- [Thesis: Nerdio on top of WVD is a 'perfect marriage'](nerdio-wvd-perfect-marriage-thesis.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
- [WVD roadmap signals from the 2019 workshop](wvd-roadmap-signals-2019.md)
- [XD7 auto-discovers installed apps; App-V replaces Citrix profiling](xd7-app-auto-discovery-and-appv.md)
