---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-10
tags: [nerdio, wvd, autoscaling, hostpool]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Static vs dynamic host pools and autoscaling (Nerdio)

How it worked in 2020 (NMW 2.3.0): Any host pool imported into Nerdio Manager for WVD from an existing Tenant or Workspace started life as a Static host pool. Static means hosts are added and removed manually through the GUI, with no autoscaling.

A Dynamic host pool is the only kind that the Nerdio autoscaling engine can drive. To get autoscaling on an imported pool you had to rebuild the static pool into a dynamic one; as of the 2.3.0 release this rebuild was fully automated rather than manual.

The four-step flow: add existing tenants/workspaces, migrate tenants into workspaces with user assignments, convert static to dynamic, then turn on and configure autoscaling.

Note: Microsoft's own power-management scripts existed but, per Bas, didn't come close to Nerdio's engine and weren't compatible with its code.

*Bron: blogpost 'Add existing WVD deployments, migrate to ARM, and enable autoscaling' (2020-08-19), basvankaam.com.*

## Verwante notities

- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [Nerdio Manager for WVD roadmap as of mid-2020](nerdio-2020-product-roadmap-snapshot.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
