---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [application-delivery, application-layering, appdisks, appdna, virtualization]
layer: rich
bron: inside-citrix-fma
---

# Application delivery: layering vs virtualisation, and AppDisks

Bas narrows application delivery to three ways but stresses there are far more flavours once you include virtualisation, layering and containerisation — he points readers to the Application Virtualization Smackdown whitepaper and rorymon.com.

AppDisks is Citrix's approach to application layering, manageable entirely from Studio, available across all XenDesktop editions (Advanced, Enterprise, Platinum) as of version 7.8. AppDNA integration with AppDisks is Platinum-only; when paired, AppDNA automatically checks whether your AppDisks (or other apps) are compatible with the target platform.

His nuance: application layering is not a direct replacement for application virtualisation — they go hand-in-hand, and in practice you'll likely use all three (base-image-installed, virtualised, and layered apps). Layering does not isolate applications; think of it as just another tool in the toolbox. And while a single master image is great, it's a utopia in most cases — don't go nuts, keep the number of images to a minimum. Less is more.

## Bron-citaten (NL, verbatim)

> Remember that, although a single master image is great to have, it is also a utopia in most cases. Just don't go nuts: keep the number of images to manage to a minimum. Less is more.

## Verwante notities

- [App-V management from Citrix Studio (XenDesktop 7.8)](app-v-in-xendesktop-7-8.md)
- [Limited AppDNA in XD7 is still a smart inclusion](appdna-in-xd7-limited-but-good-direction.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Bas's key takeaways on application delivery and layering](bas-key-takeaways-application-delivery.md)
- [Bas's questions before choosing a layering solution](bas-layering-questions-to-ask.md)
- [Bas on the pros of application layering](bas-pros-of-application-layering.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [Citrix AppDisks: application layering for golden images](citrix-appdisks-application-layering.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
- [Bas on MCS, workloads and the case for application layering](mcs-application-workloads-layering.md)
- [Citrix Studio Configuration sub-nodes](studio-configuration-subnodes.md)
