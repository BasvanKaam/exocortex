---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, host-pool, active-directory, gpo]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# NME persists machine names across reimage/rebuild

Important Nerdio Manager host-pool detail Bas calls out: when you set a machine name (prefix or pattern) for a host pool, Nerdio stores that name in its database. The machine gets built and named, and on reimage or rebuild it gets the exact same name back. This keeps AD clean, ensures all GPOs still apply, preserves whitelisting, and so on. He flags this as an important detail worth teaching.

Related host-pool notes from the same review:
- You can select any type of image when adding a host pool.
- All dropdowns are API-driven, so when Microsoft adds or removes a resource it reflects in NME automatically.
- When adding an existing host pool or workspace it's not just about adding the resource group; a vNet may also need to be added.
- Switching between directories of a different type is not possible (host pool properties).

Dated: NME UI behavior; verify against current NME Help.

*Bron: Nerdio-content 'Feedback on NME-201 exam' (Training).*

## Verwante notities

- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio Enterprise Optimization Journey (12-step framework)](nerdio-enterprise-optimization-journey.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [NME first-admin RBAC and log analytics retention savings](nme-rbac-first-admin-and-savings.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [Static vs dynamic host pools and autoscaling (Nerdio)](static-vs-dynamic-hostpools-nerdio.md)
