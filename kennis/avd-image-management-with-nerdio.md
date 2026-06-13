---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, wvd, nerdio, image-management, golden-image, automation]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# AVD/WVD Image Management Capabilities with Nerdio

Deploying WVD is the easy part; the challenge starts after, with ongoing image management. Nerdio's reusable concepts for this:

- **Reimage in place:** update existing host pools from Azure custom managed images or Shared Image Gallery images without recreating/rebuilding the pool, keeping all assignments and groups intact. No extra import step and no temporary VMs needed (cost savings).
- **Image sources:** custom managed images, Shared Image Gallery (fully integrated), or Microsoft Marketplace images, used directly to create or update host pools. Existing Azure VMs can be imported as an image/template.
- **Versioning via native Azure backup:** create versions of desktop images before changes and revert to a prior version. Back up an image while it's powered on or trigger a backup manually.
- **Image optimization on creation:** apply settings like time-zone redirection and VM time zone; auto clean up previous WVD agent or FSLogix installs when importing from a session host.
- **Multi-region:** clone a desktop image to remote Azure regions (one image into multiple regions) for session-host deployment or reimaging there.
- **Staged, scheduled updates:** schedule host-pool updates, set how many hosts update at once, define how many failures are tolerated, and notify users who may still be active. Update hosts one by one or all at once.

The workflow pattern: boot the image, make changes, sysprep, save/shut down, then schedule the staged rollout to hosts.

*Bron: Nerdio-content 'Nerdio Image Management' (Blogs).*

## Verwante notities

- [Application layering toward a zero-app golden image](application-layering-zero-apps-in-golden-image.md)
- [A six-pillar application management strategy for AVD](avd-application-management-strategy-six-pillars.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-added-value-on-cloud-pc.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Staging desktop images and auto-activation](nerdio-image-staging-auto-activation.md)
- [Moving images and AVD objects from NME to NMM via Azure tags](nerdio-nme-to-nmm-image-migration-via-tags.md)
- [Patch Tuesday: fully automated image patching in Nerdio](nerdio-patch-tuesday-image-automation.md)
- [Automating the Patch Tuesday image lifecycle in Nerdio](nerdio-patch-tuesday-image-lifecycle-method.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-value-on-top-of-cloud-pc.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
