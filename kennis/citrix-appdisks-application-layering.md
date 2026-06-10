---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, appdisks, application-layering, xendesktop]
layer: reference
bron: inside-citrix-fma
---

# Citrix AppDisks: application layering for golden images

AppDisks is Citrix's application-layering technology that lets administrators package and manage applications independently of their golden images, reducing the number of golden images required. Instead of installing an application into the golden image, the application's data is redirected into a virtual disk (a VHD or VMDK, depending on the hypervisor). Once created, an AppDisk can be assigned across multiple golden images, even across Windows versions, as long as the application itself can handle the respective Windows version.

AppDisks is available as of XenDesktop / XenApp version 7.8. It is included with all XenDesktop editions (Advanced, Enterprise, Platinum). AppDNA integration with AppDisks is for Platinum-licensed customers only; AppDNA automatically checks AppDisks for compatibility issues with the underlying OS and other installed software, and tells you what is wrong and how to correct it.

## Verwante notities

- [Application delivery: layering vs virtualisation, and AppDisks](application-delivery-layering-vs-virtualisation.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Bas's key takeaways on application delivery and layering](bas-key-takeaways-application-delivery.md)
- [Bas's questions before choosing a layering solution](bas-layering-questions-to-ask.md)
- [Bas on the pros of application layering](bas-pros-of-application-layering.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
- [Bas on MCS, workloads and the case for application layering](mcs-application-workloads-layering.md)
- [Citrix Studio console root nodes](studio-console-root-nodes.md)
