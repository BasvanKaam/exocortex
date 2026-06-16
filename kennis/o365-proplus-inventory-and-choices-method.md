---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [office-365, method, migration, deployment, whitepaper]
layer: reference
gedateerd: nee
bron: salomon-whitepaper
---

# ProPlus inventory-and-choices method before rollout

Bas van Kaam's pre-rollout checklist method from the whitepaper: before adopting ProPlus, inventory the environment and make explicit choices so nothing is overlooked. Items to decide/inventory:

- Windows or Mac OS; 32-bit or 64-bit software.
- Existing Office version, and any (VBA) macros or plug-ins, and whether they work with the newer version. Same check for Visio, Project, Teams (not part of the Office suite).
- Language packs needed.
- Whether client devices meet minimum system requirements.
- Which deployment tools are available and preferred.
- User count (licensed per user); ensure enough licenses, noting Visio and Project need separate licenses.
- Internal network capacity: roughly 1.6 GB primary files per user, ~250 MB per language pack.
- Internet access on clients (one-time activation plus a check every 30 days), and the right protocol ports open.
- Whether to update from the Office CDN (needs a stable, fast connection; account for remote locations).
- Finally, define a pilot group of users and devices meeting all requirements; have them test rollout AND application compatibility thoroughly before rolling out to the rest of the organization.

The method (inventory first, pilot before production) is durable; the specific figures are 2019-era.

*Bron: Salomon-IT 'Whitepaper'.*

## Verwante notities

- [ProPlus deployment and update tooling options](o365-proplus-deployment-and-update-options.md)
- [Office 365 ProPlus on Remote Desktop Services](o365-proplus-on-rds.md)
- [ProPlus pre-rollout inventory checklist](office-365-proplus-inventory-before-rollout.md)
- [An Office rollout is part of a wider workplace transformation](office-rollout-is-bigger-than-installing-software.md)
- [OS Migration Is More Than Swapping the OS](os-migration-is-more-than-the-os.md)
