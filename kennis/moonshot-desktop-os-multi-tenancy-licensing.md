---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [moonshot, multi-tenancy, licensing, csp, windows-desktop-os]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Delivering a desktop OS multi-tenant via dedicated Moonshot cartridges

How it worked then (2015): Microsoft licensing did not allow a Windows desktop OS to be offered from shared/multi-tenant hardware (unlike XenApp hosted shared desktops, which had been offered from the cloud for years). Moonshot offered a workaround for service providers: dedicate a full cartridge (4 nodes) exclusively to a single customer/tenant, satisfying the dedicated-hardware requirement even if the customer only needed two desktops. Bas noted Microsoft had verified this but you needed an official written statement from Microsoft permitting the specific configuration. The durable point: hardware-isolation tricks can unlock licensing models that shared virtualization cannot, at the cost of stranded capacity.

*Bron: blogpost 'HP Moonshot revisited. Well... by me anyway' (2015-06-30), basvankaam.com.*

## Verwante notities

- [Client OSes were not allowed on multi-tenant public cloud (2013 licensing)](client-os-not-allowed-multitenant-cloud-2013.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [HP Moonshot: physical one-to-one desktops (HDI) and XenApp cartridges](hp-moonshot-hdi-physical-one-to-one.md)
- [HP Moonshot as HDI: physical desktops, no hypervisor layer](moonshot-hdi-physical-no-hypervisor.md)
- [Why true Windows desktop DaaS was blocked by SPLA](splash-spla-no-true-windows-daas.md)
- [Virtual usually beats physical, but leasing changes the Moonshot math](virtual-beats-physical-but-leasing-changes-moonshot-math.md)
- [WorkspacePod is not an honest VIAB replacement (yet)](workspacepod-not-a-viab-replacement.md)
