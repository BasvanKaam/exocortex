---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [bas-takeaways, application-layering, appdisks, less-is-more]
layer: rich
bron: inside-citrix-fma
---

# Bas's key takeaways on application delivery and layering

Bas's closing takeaways for the application-layering chapter:

- He narrowed app delivery to three ways, but there are many more flavours (virtualisation, layering, containerisation). He recommends the 'Application Virtualization Smackdown' whitepaper and rorymon.com.
- AppDisks is Citrix's approach to application layering, available for all licenses; AppDNA integration is Platinum-only.
- Application layering is not a direct replacement for application virtualisation: they go hand-in-hand. In practice you'll probably use all three: base-image-installed, virtualised, and layered apps.
- Layering does not isolate applications like App-V does.
- Think of layering as 'just another tool in the toolbox to make life a little easier.'
- A single master image is great but is a utopia in most cases. His refrain: 'Just don't go nuts: keep the number of images to manage to a minimum. Less is more.'

## Bron-citaten (NL, verbatim)

> Just don't go nuts: keep the number of images to manage to a minimum. Less is more.
>
> another tool in the toolbox to make life a little easier

## Verwante notities

- [Application delivery: layering vs virtualisation, and AppDisks](application-delivery-layering-vs-virtualisation.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Bas's questions before choosing a layering solution](bas-layering-questions-to-ask.md)
- [Bas on the pros of application layering](bas-pros-of-application-layering.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [Citrix AppDisks: application layering for golden images](citrix-appdisks-application-layering.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
