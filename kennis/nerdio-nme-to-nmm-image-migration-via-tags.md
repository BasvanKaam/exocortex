---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nme, nmm, image-management, azure-tags, migration]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Moving images and AVD objects from NME to NMM via Azure tags

Bas's hands-on test notes for migrating a desktop image (and related AVD objects) from Nerdio Manager for Enterprise (NME) to Nerdio Manager for MSP (NMM), assuming both apps point at the same Azure subscription, network and resource group.

Key finding: no import/export, no special permissions, and no settings changes inside NME or NMM are needed. The only change is modifying Azure tags on the associated resources in the Azure portal. He created a new image in NME in the common resource group/network, then updated the tags on the VM, NIC, disk and image. Replace the NME version of the tags with the NMM ("WAP") version (or vice versa) and refresh the page, and the image effectively "moves" from one app to the other. (In his test he duplicated tags so it showed in both, but for a real customer/partner you replace, not duplicate — running "set as image" on one side would likely break the other, so the same image must not be used on both sides.)

What transfers vs. what doesn't:

- Transfers automatically NME -> NMM: Workspaces, Host Pools, App Groups (and assignments). NMM -> NME requires associating the Workspace; not automatic in reverse. For NME to show VMs as associated, add Azure tags (or just use Associate from within NMM).
- Does NOT transfer: Nerdio Manager and pool configuration items — autoscale configuration and history, AD and FSLogix configuration profiles (from Settings), and session time limits.

His note on effort: renaming many tags by hand is a little tedious, but it's a one-time operation and doesn't take long.

*Bron: Nerdio-content 'From NME to NMM' ((root)).*

## Verwante notities

- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [NME to NMM migration runbook (AVD)](nme-to-nmm-migration-runbook.md)
- [NMM's four customer onboarding scenarios and what each reuses](nmm-customer-deployment-scenarios.md)
