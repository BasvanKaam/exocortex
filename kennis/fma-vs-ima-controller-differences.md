---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, ima, delivery-controller, data-collector, architecture]
layer: rich
bron: inside-citrix-fma
---

# FMA Controllers differ fundamentally from IMA Data Collectors

Bas repeatedly warns not to conflate the FMA with the older IMA. Delivery Controllers (FMA) are fundamentally different from Data Collectors (IMA): no Local Host Cache, they communicate directly with the Central Site database, they do not communicate between each other, and the model is service- and agent (VDA)-based.

The deeper architectural shift: in the FMA all HDX/ICA bits and bytes are installed as part of the VDA on the Session Host and VDI VMs, while the Delivery Controller concerns itself primarily with brokering, maintaining and optimising existing sessions. Understanding how traffic flows between components in each architecture is, in his view, vital to successful troubleshooting.

## Verwante notities

- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [Delivery Controller vs. Data Collector (FMA vs. IMA)](delivery-controller-vs-data-collector-2.md)
- [The evolution of the FlexCast Management Architecture](evolution-of-the-fma.md)
- [IMA-to-FMA terminology mapping table](ima-vs-fma-terminology-mapping.md)
- [Bas's troubleshooting philosophy: master the basics before reaching for tools](troubleshooting-know-the-basics-first.md)
