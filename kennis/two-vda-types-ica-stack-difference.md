---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, ica-stack, portica, rdsh, vdi]
layer: reference
bron: inside-citrix-fma
---

# Two VDA types and the single-user vs multi-user ICA stack

Because the FMA was originally VDI-only, Citrix had to create a new server-OS VDA when XenApp joined. The key difference between the two VDA types is the underlying ICA protocol stack:

- Desktop machines: a single-user ICA stack (a.k.a. PortICA) allowing only one ICA session at a time. It includes extra HDX features such as USB and Aero redirection that are only available on single-user machines.
- Server machines: a multi-user ICA stack that extends Windows Remote Desktop Services with the HDX/ICA protocol. This is essentially the same ICA stack developed for XenApp 6.5 and earlier, with technical adjustments to make it compatible with FMA Delivery Controllers.

Depending on viewpoint there are two VDAs, or four: one for Windows desktop OS, one for Windows server OS, plus a Linux VDA covering both desktop and various server distributions. FMA fact: there is also a Linux-based VDA, and a separate HDX 3D Pro VDA for GPU acceleration.
