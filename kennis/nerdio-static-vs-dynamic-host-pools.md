---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-10
tags: [nerdio, wvd, host-pool, autoscale, concepts]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Static vs dynamic host pools in Nerdio (autoscale eligibility)

The distinction as it worked in Nerdio Manager for WVD in 2020:

Static host pools: created empty or with a fixed number of session hosts, manually controlled by the admin, NOT autoscale-capable. Can serve pooled desktops, personal desktops, or RemoteApps.

Dynamic host pools: built from a single desktop image and re-imaged automatically; when a VM is turned off by an autoscale policy it gets deleted. Autoscale can be on or off. Can serve pooled desktops, RemoteApps and single-user non-persistent desktops, but NOT personal/dedicated desktops.

The load-bearing trade-off: only dynamic pools autoscale, but dynamic pools can't do personal/dedicated desktops. Dated to the 2020 product/terminology, but the static-vs-elastic split and 'autoscale means non-persistent' constraint is a durable concept.

*Bron: blogpost 'How to: Nerdio Manager for WVD, first steps. Part two (host pools, autoscale, images)' (2020-04-16), basvankaam.com.*

## Verwante notities

- [Ephemeral disks' biggest drawback disappears with the right autoscaler](ephemeral-disks-cons-as-pros.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio autoscaling for personal/persistent desktops](nerdio-autoscaling-personal-persistent-desktops.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [NME persists machine names across reimage/rebuild](nme-hostpool-naming-persistence.md)
- [What the Nerdio autoscale engine does (NMW era)](nmw-autoscale-engine-capabilities.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
- [Static vs dynamic host pools and autoscaling (Nerdio)](static-vs-dynamic-hostpools-nerdio.md)
- [WVD App Group rules (2019)](wvd-app-groups-rules-2019.md)
- [WVD Classic to ARM migration: the two-step pattern](wvd-classic-to-arm-two-step-migration.md)
