---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop-essentials, citrix-cloud, vda, architecture]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The key line between Essentials and full Citrix Cloud: VDA placement

How it worked then (2017): the biggest architectural distinction Bas drew between XenDesktop Essentials and the full Citrix Cloud XenApp/XenDesktop services was where your VDAs could live. With the full Citrix Cloud services, VDAs could still run on-premises, in another cloud, or hybrid (your choice). Essentials was Azure-bound. Essentials also dropped some capabilities: no Workspace Environment Services and no Citrix Profile Management. You could still use HDX (including the HDX RealTime Optimization Pack for Skype for Business), StoreFront app stores, NetScaler for secure remote access, Smart Scale, and Director Platinum for advanced monitoring and analytics.

*Bron: blogpost 'Citrix XenDesktop Essentials - all facts listed!' (2017-03-02), basvankaam.com.*

## Verwante notities

- [Citrix Managed Desktop: single-bill DaaS on Citrix-managed Azure](citrix-managed-desktop-model-2019.md)
- [Workspace Cloud lacked an on-prem control plane in 2015](citrix-workspace-cloud-control-plane-2015.md)
- [Citrix Workspace Cloud (CWC): a managed control plane over the FMA](citrix-workspace-cloud-overview.md)
- [CWC as a near-DaaS workaround for Microsoft desktop-OS licensing](cwc-desktop-os-daas-licensing.md)
- [Machine Creation Services essentials](machine-creation-services-essentials.md)
- [Cloud, and Citrix especially, is almost always more expensive than on-prem](position-citrix-cloud-is-almost-always-pricier-than-on-prem.md)
- [Citrix XenDesktop Essentials: what it was and what the price covered](xendesktop-essentials-what-it-was.md)
