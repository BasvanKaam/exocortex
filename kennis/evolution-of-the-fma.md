---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, history, xenapp, xendesktop, ima]
layer: rich
bron: inside-citrix-fma
---

# The evolution of the FlexCast Management Architecture

Both XenApp and XenDesktop are built on the FlexCast Management Architecture (FMA), and Bas expects that to remain true for years. The FMA was first introduced with XenDesktop 5.0 in December 2010 (before that XenDesktop used the Independent Management Architecture, IMA). It was always meant as the next-generation architecture, offering enhanced scalability, robustness, flexibility and manageability over the IMA, and was initially built with VDI in mind. The FMA itself is a Microsoft .NET-based architecture built on the WCF (Windows Communication Foundation) framework, with .NET apps running in the Common Language Runtime.

XenApp joined the FMA on 26 June 2013 — the GA date of XenDesktop 7.0 — which required a new Server VDA. At that point XenApp was no longer a separate product and Citrix stopped developing 6.5. Bas calls this a mistake: Citrix listened and reintroduced XenApp and XenDesktop as separate products with version 7.5, and he doubts they will repeat the error.

## Bron-citaten (NL, verbatim)

> Luckily, Citrix listened and reintroduced XenApp and XenDesktop as separate products with the release of version 7.5. I don't think they will make a mistake like that again.

## Verwante notities

- [Bas's take: the Current Release isn't really new](bas-current-release-not-really-new.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [Delivery Controller vs. Data Collector (FMA vs. IMA)](delivery-controller-vs-data-collector-2.md)
- [FlexCast delivery technology, worker types and delivery models](flexcast-delivery-models-and-worker-types.md)
- [FMA architectural casualties: Zones, LHC and Worker Groups removed then re-added](fma-architectural-changes-zones-lhc-removed.md)
- [FMA evolution key dates](fma-evolution-key-dates.md)
- [FMA foundation: .NET, WCF, CLR and just-in-time compilation](fma-foundation-dotnet-wcf-clr.md)
- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
- [FMA Controllers differ fundamentally from IMA Data Collectors](fma-vs-ima-controller-differences.md)
- [The origin of Citrix and the ICA protocol](history-of-citrix-and-ica.md)
- [IMA-to-FMA terminology mapping table](ima-vs-fma-terminology-mapping.md)
- [The nine main FMA components and the XenDesktop Site definition](nine-main-fma-components.md)
- [XenApp folded into the FMA: the Excalibur / XenDesktop 7.0 moment](xenapp-joins-fma-excalibur-2013.md)
