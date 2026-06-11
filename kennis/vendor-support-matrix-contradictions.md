---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [support, lync, vendor-matrix, troubleshooting]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Citrix says supported, Microsoft says not: reading two support matrices at once

A durable lesson from a 2015 Lync-on-XenApp investigation: when a feature spans two vendors, their support statements can directly contradict each other. Citrix's eDocs listed XenApp 6.x/7.x with published (hosted shared) desktops as supported for the Lync VDI plug-in; Microsoft's documentation stated Remote Desktop Sessions via RDS or Citrix XenApp were NOT supported, and the two disagreed on which client and VM operating systems qualified (Windows 7 SP1 vs Windows 8, etc.).

The practical takeaway: "technically it works" and "you get support when you need it" are two different questions. Verify support against the actual vendor source rather than assuming, and accept that you may have to make a judgement call ("decision time") when the matrices conflict.

*Bron: blogpost 'Citrix XenApp & Microsoft (online) Lync... Things to be aware of. My findings!' (2015-03-29), basvankaam.com.*

## Verwante notities

- [Using CentOS 6.6 to test the Citrix Linux VDA (unsupported but code-close to RHEL)](linux-vda-centos-unsupported-but-usable-for-testing.md)
- [Delivering Lync in a XenApp hosted shared desktop: generic vs optimized HDX](lync-xenapp-delivery-options.md)
- [Features Server VDI cannot do](server-vdi-unsupported-features.md)
- [Don't make concessions on end user experience when delivering Lync](stance-lync-online-xenapp-concessions.md)
- [Run a CDF trace before you contact Citrix Support](trace-before-you-call-citrix-support.md)
