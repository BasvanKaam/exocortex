---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [base-image, golden-image, image-management, lifecycle, vdi, rdsh]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# The 'big bad image' problem: why everything in the base image hurts

Apps that can't be virtualized or replaced end up in the base/golden image, and that is not something to get excited about. The costs: every patch or update has to be made on the production image; unused apps still all need patching; you can't easily run multiple versions of the same software side by side; images can balloon to hundreds of GB; and every image change typically triggers a full retest-and-accept cycle under change management, which takes a day or two minimum even when fast. Apps that need weekly or twice-weekly updates make a once-a-month image cycle unacceptable. This pushes teams toward multiple silos/images per department, when the goal should be 'less is more'. The principle is durable even though the specific tooling has moved on.

*Bron: blogpost 'Application Layering questions? I got answers. Graphical cheat sheet included!' (2015-12-01), basvankaam.com.*

## Verwante notities

- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [Application virtualisation tops out around 70-80% in practice](app-virtualisation-ceiling-70-80.md)
- [Azure Ephemeral OS disks for stateless WVD workloads](azure-ephemeral-os-disks.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [Why MCS image updates matter: every master VM is re-copied to every datastore](mcs-image-update-repeats-full-copy.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [Non-persistent plus layering = the best of both worlds](non-persistent-feels-persistent-with-layering.md)
- [If most VDIs are non-persistent, why aren't more apps virtualised?](non-persistent-vs-app-virtualisation-surprise.md)
- [Pooled vs dedicated desktops: the durable trade-off](pooled-vs-dedicated-desktops.md)
- [App layering that keeps the base image clean is the right model for AVD](positie-app-layering-keeps-the-image-clean.md)
- [Layering and virtualization are partners, and the cons are soon forgotten](positie-layering-and-virtualization-coexist.md)
- [MCS vs PVS is done to death; pick a lens and stress-test the choice](positie-mcs-not-vs-pvs.md)
- [Start from a fresh image rather than reusing legacy (Citrix) images](start-from-a-fresh-image.md)
- [Even with managed WVD, the customer still owns the base image](wvd-customer-still-owns-the-base-image.md)
