---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix-cloud, xendesktop-essentials, licensing, cost, daas]
layer: reference
gedateerd: ja
bron: salomon-it-blog
---

# Citrix Cloud / Essentials commercial reality vs the cloud promise

Bas's technical correction (Salomon era, post the Citrix rename) to claims that 'Citrix in the cloud' is cheap and elastically scalable. The licensing structure undercuts the cloud story:

- **You must buy at least 25 licenses for Essentials**, and for both options (the XenDesktop Service and Essentials) you commit for a minimum of one year. The headline price often shown is even based on a three-year term.
- That kills much of the elastic scaling argument: scale-down does not lower your bill because you are locked into the licenses (1 or 3 years, minimum 25). The seasonal-worker cost-saving argument therefore does not hold.
- **Why:** these offerings were 'not born in the cloud' but a lift-and-shift of the existing infrastructure (Citrix was working on it at the time), so the cloud mindset is partly missing.
- **Essentials is operationally fragmented:** you need a separate Azure subscription, a separate Citrix Cloud account, you own the image, everything is managed and billed separately, you configure the cloud connectors yourself (duplicated), a NetScaler/ICA proxy is required, and more. Lots of room for Citrix to improve.
- **Naming pedantry:** it is not 'XenDesktop', it is the XenDesktop Service or XenDesktop Essentials (materially different), and after the latest rename it is Virtual Apps and Desktops.
- **VDI terminology:** VDI is a Virtual Desktop Infrastructure; do not use 'VDI' to refer to a single VM. And VDI is only one of the delivery options on Azure, not the only one, despite how some copy reads.

Source: Bas van Kaam, internal feedback document on ComeGetIT, Salomon IT era.

*Bron: Salomon-IT 'Feedback op ComeGetIT' (Salomon Blogs).*

## Verwante notities

- [Bas's blog house-style and platform-hygiene rules (ComeGetIT review)](bas-blog-house-style-and-platform-hygiene.md)
- [The Cloud Is Not Automatically Cheaper, And 'No Upfront Investment' Is Often False](cloud-is-not-automatically-cheaper.md)
- [Cloud, and Citrix especially, is almost always more expensive than on-prem](position-citrix-cloud-is-almost-always-pricier-than-on-prem.md)
- [RDSH vs VDI vs DaaS vs WVD: Single-User and Multi-User Explained](rdsh-vdi-daas-wvd-explained.md)
- [When Citrix still makes sense (and when an alternative is better)](when-citrix-still-makes-sense.md)
