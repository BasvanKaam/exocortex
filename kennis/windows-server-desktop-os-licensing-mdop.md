---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [microsoft, licensing, volume-licensing, mdop, app-v]
layer: reference
bron: inside-citrix-fma
---

# Windows server/desktop OS licensing and App-V (MDOP)

Base OSs also need licensing. A Windows **server** license lets you install the server OS on one machine; you also need **server client access licenses** per user for services like file sharing and printing. **Desktop** OS licenses work similarly under Volume Licensing but need no additional CALs. Different Volume Licensing programs apply depending on organization size, and some can include Software Assurance.

The Microsoft Desktop Optimization Pack (**MDOP**) provides virtualization technologies including **App-V**, often used with both XenApp and XenDesktop. It is not free — a separate subscription available to Microsoft SA customers. Streaming App-V to VDI virtual desktops requires one MDOP license per client device; streaming to XenApp (RDSH) servers requires no additional licenses (already covered by the RDS CAL).
