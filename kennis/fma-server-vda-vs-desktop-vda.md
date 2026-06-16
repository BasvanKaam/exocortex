---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, vda, portica, broker, rdsh, xendesktop-7]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FMA Server VDA vs Desktop VDA: multi-session and direct controller comms

How it worked then (XenDesktop 7 / FMA 2.0): the introduction of XenDesktop 7 integrated XenApp under the FMA and brought a brand-new, optional, relatively lightweight Server VDA, the first time installing an agent onto a XenApp server wasn't all-or-nothing. Key differences from the Desktop VDA: the Server VDA accepts and manages multiple user sessions at once (the RDSH model), where the Desktop VDA (PortICA) handles only one ICA session. Server VDAs communicate directly and exclusively with the Delivery Controller (via the Broker Agent) and do not need access to the central Site SQL database or the license server. The underlying OS of the RDSH server need not match the Delivery Controller, and a Site can mix OSes.

*Bron: blogpost 'An in-depth look at the Citrix FMA Server VDA… The one that (almost) got away!' (2015-12-16), basvankaam.com.*

## Verwante notities

- [Excalibur's Catalog + Delivery Group model (how XD7 worked at launch)](excalibur-catalogs-delivery-groups-model.md)
- [Excalibur merges XenApp and XenDesktop onto FMA](excalibur-merges-xenapp-xendesktop-fma.md)
- [The Server VDA is the component everyone overlooked](positie-server-vda-overlooked.md)
- [Server VDA internals: Broker Agent, ICA stack, StackControlService](server-vda-internals-fma.md)
- [Server VDA internals: StackControlService bridges Broker Agent and ICA stack](server-vda-internals-stackcontrolservice.md)
- [Server VDI vs Hosted Shared Desktop in XenDesktop 7](server-vdi-vs-hsd.md)
