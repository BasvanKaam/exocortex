---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, xenapp, xendesktop, architecture]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FMA unified XenApp and XenDesktop on one architecture

How it worked then (2014, version 7.5): XenApp and XenDesktop were merged onto the same FlexCast Management Architecture (FMA), the successor to the older IMA. Because both products shared the same underlying architecture they were largely identical: same Studio and Director management consoles (including EdgeSight and NetScaler Insight), same HDX portfolio with 3D support, same provisioning via MCS/PVS. The key difference stayed at the ICA stack: XenApp remained multi-user aware (multi ICA stack), XenDesktop stayed single-user (single ICA stack). With XenDesktop 7.5 the XenApp 7.5 bits were included for seamless integration.

*Bron: blogpost 'Citrix XenDesktop 7.5... What's new?!' (2014-01-30), basvankaam.com.*

## Verwante notities

- [Excalibur merges XenApp and XenDesktop onto FMA](excalibur-merges-xenapp-xendesktop-fma.md)
- [IMA-to-FMA terminology: Farm to Site, Data Collector to Delivery Controller](ima-to-fma-terminology-map.md)
