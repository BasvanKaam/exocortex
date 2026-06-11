---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenapp, excalibur, storefront, migration]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenApp roles removed/replaced moving to Excalibur (2013 mapping)

Bas's role-by-role comparison of XenApp 6.5 against the Excalibur Tech Preview:
- Web Interface -> replaced by StoreFront
- Receiver StoreFront role -> now just 'StoreFront'
- EdgeSight -> redesigned as HDX EdgeSight, integrated into the FlexCast 2.0 console and leveraged by Director
- SmartAuditor, Power and Capacity Management -> no longer available
- Single Sign-On -> part of StoreFront
- Provisioning Services and Merchandising Server -> still separate products
- Shadowing -> gone, replaced by Director using Microsoft Remote Assistance
- IMA -> replaced by XenDesktop's FMA
- Worker Groups, Zones, Data Collectors, Load Balance/Zone Preference policies -> gone; it is now one big Site

Dated, but a useful historical record of what the XenApp-to-FMA transition dropped.

*Bron: blogpost 'Post Excalibur remarks' (2013-04-10), basvankaam.com.*

## Verwante notities

- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [Excalibur is XenDesktop on steroids and here to stay (April 2013)](excalibur-is-here-to-stay.md)
- [Excalibur is XenDesktop-centric and steals XenApp's thunder (April 2013)](excalibur-steals-xenapp-thunder.md)
- [Positie: Citrix was inexplicably late adding delegated admin to XenDesktop](positie-citrix-late-with-xendesktop-delegated-admin.md)
