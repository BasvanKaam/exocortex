---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, desktop-images, scripted-actions, change-management]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# Staging desktop images and auto-activation

The controlled-rollout method Bas teaches for updating production images. By default a new desktop image version is immediately activated for production host pools - staging breaks that so you can test first.

Staged images let you: test changes before activation in production; schedule automatic activation after a set period; or activate manually if testing succeeds.

Considerations:
- Activating an image automatically updates all associated host pools (via auto-scale and scheduled tasks).
- Older image versions are purged based on your 'Current Image Action' configuration; older versions can remain available for re-imaging existing hosts.
- 'Set as Image' scripted actions run on a clone of the image source VM, not the source itself. Best practice: schedule updates for the source VM first, then run 'Set as Image' after updates land.

Decision rule he gives: predictable environments can use auto-activation; dynamic environments should keep a hands-on review and approval step (know your patching schedule like Patch Tuesday, leave time for QC and LOB application testing). Scripted actions here are about consistency, compliance and repeatability - 'focus on outcomes rather than engineering'. dated:true.

*Bron: Nerdio-content 'PRESENTER_Enterprise_Foundations_v4.0' (Training).*

## Verwante notities

- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [Patch Tuesday: fully automated image patching in Nerdio](nerdio-patch-tuesday-image-automation.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
