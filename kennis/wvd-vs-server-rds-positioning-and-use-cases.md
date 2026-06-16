---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [wvd, rds, use-case, gpu, scaling, azure]
layer: reference
gedateerd: ja
bron: salomon-wvd
---

# WVD versus server RDS: positioning and primary use-cases

From Bas's session script (2019). How he positioned WVD against existing server-based RDS:

**Scaling.** Nearly, but not quite, the same density as 2016/2019 server RDS — roughly 20% lower.

**Why single-user / dedicated matters.** No shared resources: you can dedicate more CPU and memory per user than on a shared server OS, get better GPU support (relevant for CAD/CAM), and apply tighter security restrictions.

**Operational benefits.** No backend management (Microsoft handles it); everything you do is central; accessible anytime/anywhere over the internet, from any device, good for remote/branch locations. Pay for what you use — turn off means no cost for the underlying resources. Start small, end (very) large. "Select, click, done."

**Office/integration.** Tight Office 365/OneDrive integration, Azure AD conditional access, workplace co-located with the data. Optimized for Office ProPlus, largely thanks to the FSLogix acquisition (installs the needed plugins, codecs, packs); ProPlus is not supported on e.g. Server 2019.

**Ecosystem.** Rich partner ecosystem integrated as best-of-breed: Citrix, CloudJumper, FSLogix, Lakeside, Liquidware, People Tech Group, ThinPrint. Citrix's own future move: a DaaS layer on top of WVD; Microsoft bought FSLogix 100% for WVD.

**Use-cases:** first steps into Azure (start small), Windows 7 support + security updates during migration to Windows 10, DaaS/VDI desktops, RemoteApp publishing, single and multi-user sessions, traditional and modern apps.

*Bron: Salomon-IT 'MCS sessie' (WVD).*

## Verwante notities

- [In a hybrid world, app virtualization beats desktop virtualization](app-virtualization-over-desktop-virtualization-in-hybrid.md)
- [Microsoft deliberately leaves WVD management gaps to partners](positie-microsoft-leaves-wvd-management-to-partners-on-purpose.md)
