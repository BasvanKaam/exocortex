---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [microsoft, rds, cal, xenapp, xendesktop, licensing]
layer: reference
bron: inside-citrix-fma
---

# Microsoft RDS CALs and the XenApp vs XenDesktop split

When Microsoft RDS (Remote Desktop Services, formerly Terminal Services) is used to deliver apps or desktops, it must be licensed with **RDS CALs** (per user or device). XenApp runs on top of RDS technology and therefore needs RDS CALs. This does not apply to XenDesktop VDI, though RDS technology can also serve desktop-OS VMs on Windows Server 2012/2016 (Microsoft VDI), in which case both VDA and RDS licenses are needed.

Key rule: **Microsoft RDS licenses are needed with Citrix XenApp, not XenDesktop. Microsoft VDA licenses are needed with Citrix XenDesktop, not XenApp.**

Side note: when XenApp is used only to stream packaged applications down to a virtual or physical desktop, no RDS CALs are needed because no actual resources are used on the RDSH server.
