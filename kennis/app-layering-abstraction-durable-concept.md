---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [app-layering, app-virtualization, flexapp, concept]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Application layering: abstract the app from the OS

A durable EUC concept Bas restates here. Managing one or many images with dozens of installed apps has never been easy, regardless of vendor (Citrix, Microsoft, VMware). Application layering and application virtualization create an abstraction layer of the application that can be attached to the OS on-demand, so apps can be updated or changed without interrupting users. The contrast: when apps are installed directly into an image (as native AppStream does), every update means opening the image, changing, saving, publishing, informing users, typically out of office hours, with no separation between app and OS. Layering (e.g. FlexApp redirecting bits to a portable VHD) restores flexible, lower-touch app management. The concept predates and outlives any single product.

*Bron: blogpost 'AWS launched AppStream 2.0, here's how Liquidware adds some 'magic' on top' (2019-05-08), basvankaam.com.*

## Verwante notities

- [Framing: keep application layering and application virtualization distinct](app-layering-not-app-virtualization.md)
- [Application layering complements, does not replace, app virtualization](application-layering-vs-virtualization.md)
- [How AWS AppStream 2.0 streams apps (2019)](appstream-fleets-image-builder.md)
- [Cloud-native does not fix application management](appstream-management-not-solved-positie.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [Stance: container concepts carry over from Docker/Linux to Windows](containers-concepts-durable-over-platform.md)
- [FlexApp 6.5: filter drivers replace symbolic links, broadening layering support](flexapp-filter-driver-vs-symbolic-links.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
- [App attach is rebranded layering, but Microsoft's marketing will make it win](msix-app-attach-marketing-will-make-it-popular.md)
- [Non-persistent plus layering = the best of both worlds](non-persistent-feels-persistent-with-layering.md)
- [Windows apps are 'traditional', not 'legacy'](windows-apps-traditional-not-legacy.md)
