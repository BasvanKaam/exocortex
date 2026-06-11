---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, application-streaming, aie, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix Streaming Profile and AIE Data Paths

Where data lived inside Citrix's virtualized (streamed) application environment:

**Citrix streaming profile:**
- Running-app user data: appsdata\citrix\radecache\suite\device\c
- Virtual application install files: program files\citrix\radecache\suite\device\c

**Application in an AIE (Application Isolation Environment):**
- Running-app user data: appsdata\citrix\AIE\(name of AIE)\device\c
- Application install files: program files\citrix\AIE\(name of AIE)\device\c

*Bron: Core Knowledge doc 'Citrix General Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Framing: keep application layering and application virtualization distinct](app-layering-not-app-virtualization.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Citrix XenApp Lineage and Client Types](citrix-xenapp-lineage-and-clients.md)
- [Excalibur drops Citrix Profiling (app streaming) for App-V (2013 Synergy news)](excalibur-drops-profiling-for-appv.md)
- [VAS Application Virtualization Delivery Flow](vas-application-virtualization-flow.md)
