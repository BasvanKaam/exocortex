---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, image-management, patch-tuesday, fslogix, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Automating the Patch Tuesday image lifecycle in Nerdio

Bas's worked example of the end-to-end patch/image cycle in Nerdio, as he sets it up in the field:

1. Schedule recurring image updates a chosen number of days after Patch Tuesday (the second Tuesday of the month). Each month Nerdio updates the chosen image with the latest patches.
2. The same automated action commits changes to the image and handles the sysprep process; complexity is hidden from the admin.
3. Apply the updated, sysprepped image to a test hostpool using the same scheduling mechanism, re-imaging hosts one by one or in bulk, then validate: do apps still work, any driver issues, performance checks.
4. Nerdio first backs up critical components and integrates with the Azure Compute Gallery, so rolling back to a previous image version is always optional.
5. After testing passes, roll the image out to production hostpools with the same mechanisms.

He also describes building an entire AVD environment from scratch (multiple hostpools and machines per hostpool, with image(s), applications, FSLogix, auto-heal, and ongoing scaling/management logic) in roughly 1-2 hours, which is the mechanism Nerdio uses for a customer Proof of Value; later use-cases (HR, design, sales) are handled the same way.

Scaling profiles: preconfigured, reconfigurable, clonable scaling logic applied to existing or newly built hostpools. Creating a hostpool takes ~15 seconds; apply a pre-created autoscale profile, save and close. Alternative autoscale configs can target specific seasons (summer, Christmas), bank holidays, days or day-ranges, with adjustable aggressiveness on shutdown/removal.

First-time setup of the patch automation: he reports ~60 seconds for himself, 3-5 minutes for a first-timer with no instructions (tested in real life). Dated: tied to Nerdio's product behavior and AVD/W365 specifics circa this writing.

*Bron: Nerdio-content 'Notes from the Field (CTO) – The cherry on top!' (Blogs).*

## Verwante notities

- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [AVD / Windows 365 Discovery Questions (Bas's Talking Points)](avd-w365-discovery-questions.md)
- [Method: Agree PoC Success Criteria Up Front](method-poc-success-criteria.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Patch Tuesday: fully automated image patching in Nerdio](nerdio-patch-tuesday-image-automation.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [Zero Trust extras: patching cadence and CIS-hardened images](zero-trust-hardening-extras-patch-cis-images.md)
