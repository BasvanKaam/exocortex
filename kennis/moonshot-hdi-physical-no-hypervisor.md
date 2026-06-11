---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [hp-moonshot, hdi, vdi, workspacepod, sanbolic]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# HP Moonshot as HDI: physical desktops, no hypervisor layer

How it worked then (2015): in the WorkspacePod context, HP Moonshot (m700 cartridge) delivered desktops where all resources are physical and there is no hypervisor layer in between. In Moonshot terms this is called HDI (Hosted Desktop Infrastructure) rather than VDI, precisely because it is one-to-one physical hardware.

The Moonshot + Sanbolic 'warp drive' WorkspacePod config could manage up to three HP Moonshot chassis (3 x 180 nodes = 540 total), plus three SL4540 Proliant storage servers running Sanbolic for core infrastructure. The trade-off Bas highlights: physical one-to-one hardware gives an excellent user experience, but loses the flexibility, setup ease and management features that come with virtualization.

*Bron: blogpost 'Citrix kills VDI-in-a-Box and the Sanbolic acquisition - my thoughts' (2015-01-30), basvankaam.com.*

## Verwante notities

- [HP Moonshot: physical one-to-one desktops (HDI) and XenApp cartridges](hp-moonshot-hdi-physical-one-to-one.md)
- [HP Moonshot is converged but not truly web-scale](hp-moonshot-is-not-web-scale.md)
- [Delivering a desktop OS multi-tenant via dedicated Moonshot cartridges](moonshot-desktop-os-multi-tenancy-licensing.md)
- [Bas: companies are swinging back from virtual/cloud to physical](swing-back-from-virtual-to-physical-2018.md)
- [Virtual usually beats physical, but leasing changes the Moonshot math](virtual-beats-physical-but-leasing-changes-moonshot-math.md)
- [WorkspacePod is not an honest VIAB replacement (yet)](workspacepod-not-a-viab-replacement.md)
