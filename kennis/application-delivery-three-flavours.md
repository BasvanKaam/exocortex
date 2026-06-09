---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [application-delivery, app-v, appdisks, application-layering, locally-installed]
layer: reference
bron: inside-citrix-fma
---

# Three flavours of application delivery in XenDesktop/XenApp

Bas distinguishes application *delivery* (the mechanism used after an app is published) from merely publishing an app. There are three main flavours (he acknowledges there are more):

- **Locally installed applications**: installed as part of the base image (MCS and/or PVS) of an RDSH/VDI deployment, then published to users. They start from the base image using local compute resources. The 'master image' can also just be a single virtual or physical machine with a VDA installed.
- **True application virtualisation** using Microsoft App-V (or ThinApp, etc.). App-V is the favourite and is supported and advised by Citrix; XenDesktop 7.8 added nice App-V integration enhancements to Studio and the FMA.
- **Citrix AppDisks**: Citrix's application-layering technology, introduced with XenDesktop/XenApp 7.8 and available in all editions. Other application-layering vendors are also options.

FMA fact: Bas deliberately says 'true' application virtualisation because solutions like XenApp are also often called application virtualisation, so it is a matter of perspective.
