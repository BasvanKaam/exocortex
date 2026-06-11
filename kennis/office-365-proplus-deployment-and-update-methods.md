---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [office-365, deployment, odt, sccm, intune, euc]
layer: reference
gedateerd: nee
bron: salomon-whitepaper
---

# ProPlus deployment and update method choices

The install/update options Bas lays out, chosen on the basis of existing toolset and network capacity (a combination is allowed):
- SCCM Current Branch with local distribution points.
- Direct from the cloud via the Office CDN plus the Office Deployment Tool (ODT).
- ODT with local distribution points.
- Cloud-managed, letting users or admins install.
- Other tools such as Intune.

For updates: automatic via the Office CDN (the default), via SCCM, via ODT, via another tool like Intune, or manual reinstall. ODT and/or Group Policy are the usual way to configure the desired update settings. Microsoft recommends automatic updating, but in practice organizations want more control.

*Bron: Salomon-IT 'Whitepaper - Ofifce 365 ProPlus implementeren en onderhouden - gecorrigeerd - Copy'.*

## Verwante notities

- [ProPlus deployment and update tooling options](o365-proplus-deployment-and-update-options.md)
- [ProPlus pre-rollout inventory checklist](office-365-proplus-inventory-before-rollout.md)
- [ProPlus diagnostic data and privacy controls](office-365-proplus-privacy-controls.md)
- [Office 365 ProPlus update channels](office-365-proplus-update-channels.md)
- [Office 365 subscription families and plans](office-365-subscription-families-and-plans.md)
- [Organizations want control over updates, not full automation](position-control-updates-dont-fully-automate.md)
