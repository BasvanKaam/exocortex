---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, image-management, fslogix, compute-gallery]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# NME image management: prefer the compute gallery over the source VM

Durable Nerdio Manager image-management knowledge from Bas's review:

- Recommendation: use the Azure compute gallery as much as possible rather than committing changes to the image source VM. If you only have a source VM and need to reimage a host pool, you must revert the source VM to an older state, create a new image object, and reimage, which is slow. With the gallery you can reimage a host pool instantly with a previous version, and you can replicate image objects to other regions. Doing both (source VM for safe keeping plus gallery for fast reimaging) is likely the best option.
- Importing images: you can import existing images (distinct from an existing VM) that live in the Azure environment NME is installed into; you just need the resource group holding the image linked to Nerdio. Existing images from your compute gallery can also be imported.
- Replicas: a replica count is for building/cloning VMs in parallel, not backup. Microsoft advises roughly 1 replica per 20 VMs in a host pool (e.g. a 200-VM pool needs ~10 replicas to run smoothly).
- Backup: when image-VM backup is enabled and configured, you also get the option to back up the VM before starting it.
- FSLogix agent: it ships on pooled (single-user) images too, not just multi-session, the agent is not multi-user-specific.
- Multi-session compatibility: there is a VDI agent for multi-session, so the blanket claim that certain apps (e.g. Zscaler) only work on single-user VMs is not reliably true. Verify per app.
- CIS hardened images are available as an option.

Dated: NME UI/behavior and Microsoft's replica guidance can change; verify against current NME Help and Microsoft Learn.

*Bron: Nerdio-content 'Feedback on NME-201 exam' (Training).*

## Verwante notities

- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [FSLogix: the three core technologies after the Microsoft acquisition](fslogix-three-core-technologies.md)
- [Nerdio Adoption & Management Framework: Five Foundational Elements](nerdio-adoption-management-framework.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Scoping desktop images: what to avoid on an image source VM](nerdio-image-source-vm-scoping-pitfalls.md)
- [Staging desktop images and auto-activation](nerdio-image-staging-auto-activation.md)
- [Moving images and AVD objects from NME to NMM via Azure tags](nerdio-nme-to-nmm-image-migration-via-tags.md)
- [Patch Tuesday: fully automated image patching in Nerdio](nerdio-patch-tuesday-image-automation.md)
- [Automating the Patch Tuesday image lifecycle in Nerdio](nerdio-patch-tuesday-image-lifecycle-method.md)
- [How Bas reviews Nerdio L&D content as SME](nme-course-content-review-method.md)
- [NME persists machine names across reimage/rebuild](nme-hostpool-naming-persistence.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [Start from a fresh image rather than reusing legacy (Citrix) images](start-from-a-fresh-image.md)
- [Zero Trust extras: patching cadence and CIS-hardened images](zero-trust-hardening-extras-patch-cis-images.md)
