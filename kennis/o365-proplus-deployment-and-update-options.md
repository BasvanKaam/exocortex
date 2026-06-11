---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [office-365, proplus, deployment, sccm, odt, intune, whitepaper]
layer: reference
gedateerd: ja
bron: salomon-whitepaper
---

# ProPlus deployment and update tooling options

From the whitepaper. Install/update method depends on current toolset and network capacity. Options:

- SCCM (Current Branch) with local distribution points.
- Direct from the cloud via the Office CDN plus the Office Deployment Tool (ODT).
- ODT with local distribution points.
- Cloud-managed, letting users or admins install Office 365.
- Any distribution form is allowed, including Intune; combinations are permitted.

Updates can run: automatically via the Office CDN (the default); via SCCM (download to local distribution points, then distribute/install); via ODT similarly; via another tool such as Intune; or manually by installing a new ProPlus version. In practice Bas notes organizations rarely use fully automatic updating because they want more control, and ODT and/or Group Policy are typically used to configure settings.

Supporting tools he calls out: the Readiness Toolkit reports add-ins, plug-ins, macros and compatibility issues (scans Word, Excel, PowerPoint, Outlook, Access, Project, Visio, Publisher; supports Office versions back to 2003) and recommends fixes. Microsoft recommends removing older Office versions before installing ProPlus; the ODT can help. Time-bound to 2019 tooling.

*Bron: Salomon-IT 'Whitepaper'.*

## Verwante notities

- [ProPlus inventory-and-choices method before rollout](o365-proplus-inventory-and-choices-method.md)
- [Controlling ProPlus diagnostic data and connected services](o365-proplus-privacy-controls.md)
- [Office 365 ProPlus Update Channels model](o365-update-channels-model.md)
- [ProPlus deployment and update method choices](office-365-proplus-deployment-and-update-methods.md)
- [Organizations want control over updates, not full automation](position-control-updates-dont-fully-automate.md)
- [Windows 10 servicing branches and deployment rings](windows10-servicing-branches-rings.md)
