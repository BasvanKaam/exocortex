---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nme, avd, patch-management, image-management, automation]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Patch Tuesday: fully automated image patching in Nerdio

Bas's go-to explainer for how Nerdio Manager removes the operational burden of monthly patching for AVD and Windows 365 images. His framing: keeping machines current is a resource-intensive, out-of-hours, expensive task and a security risk; many companies are months behind. Once configured, the whole process takes roughly 60 seconds of admin time.

The workflow he walks through:

1. Image management runs through Nerdio's Scripted Actions integration, so pulling the updates is fully automated. You set the exact start date, time and time zone, plus the number of days after Patch Tuesday you want updates applied to a chosen image.
2. Enable the built-in backup, use Azure Compute Gallery integration for geographic distribution, and set your preferred number of replicas. Save and close — the steps repeat every month. As part of the run, changes are committed, the image object is created and sysprepped, ready to go.
3. Use the re-size / re-image option on the host pool you want to test against and select the patched image. For a bigger pool, re-image multiple machines at once in batches, blocking new logons during the process and warning active users to save work. Schedule it two days after Patch Tuesday, set execution a few hours later so Nerdio has time to create the image object, save and close.

Result: a fully patched, sysprepped image (with a backup of the original), applied to a test host pool, with replicas in your Azure Compute Gallery — automated, repeated monthly, configured per image/host pool. He demonstrated this live at a MicroHack event where participants who had never seen Nerdio completed it within minutes.

His tagline for it: "the easy button."

*Bron: Nerdio-content 'Aankondigingen-thisismine' ((root)).*

## Verwante notities

- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Staging desktop images and auto-activation](nerdio-image-staging-auto-activation.md)
- [Automating the Patch Tuesday image lifecycle in Nerdio](nerdio-patch-tuesday-image-lifecycle-method.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
