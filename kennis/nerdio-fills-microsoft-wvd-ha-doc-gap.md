---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-10
tags: [nerdio, wvd, high-availability, opinion]
bron: basvankaam-blog
---

# Nerdio shines where Microsoft's WVD HA docs are missing

Dec 2020. Bas points out that if you search for Microsoft documentation on setting up Availability Zones for WVD specifically, "you are unlikely to find any" - only community PowerShell-heavy posts exist, nothing official from Microsoft on WVD. His framing: "This is where Nerdio shines." In NMW, Availability Sets is a single checkbox for the whole deployment, and Availability Zones can be toggled per host pool with a mouse click.

He also makes a resilience-of-the-tool argument: once set up via NMW, the environment keeps working even if NMW itself becomes unavailable (sessions still brokered, data still accessible), because NMW integrates directly with native Azure/WVD rather than sitting in the data path. The caveat he's honest about: while NMW is down, scaling/healing of hosts must be done manually in the Azure portal.

He closes by reframing NMW's fast rebuild time as a DR metric: NMW setup in ~45 min, onboarding an existing WVD env in 15-20 min, full recovery within 1-5 hours - 'Not a bad RTO, is it?'

*Bron: blogpost 'How to Make Your 1,000+ User WVD Deployment Highly Available' (2020-12-07), basvankaam.com.*

## Verwante notities

- [Azure Availability Sets vs Availability Zones](azure-availability-sets-vs-zones.md)
- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [Framing: the product's job is hiding complexity](hiding-complexity-is-the-product.md)
- [Nerdio Manager for WVD deploys into your own Azure tenant](nerdio-manager-wvd-deploys-in-your-tenant.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
