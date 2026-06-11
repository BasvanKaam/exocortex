---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [application-layering, app-virtualization, app-v, thinapp, vdi, rdsh]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Application layering complements, does not replace, app virtualization

App virtualization (App-V, ThinApp) and application layering are often confused, but they solve different problems and go hand in hand. The hard limit of app virtualization is coverage: on average only 50-60% of applications can be virtualized (per Project VRC / Virtual Reality Check figures of the time). A mid-to-large company easily has a few hundred apps, so even at 60% you are left with dozens, potentially hundreds, of apps that must be presented some other way. Cloud apps help but mostly apply to newer apps and won't fit every use case; legacy apps can't be swapped out easily. Application layering is a way to deliver that remaining tail without baking it into the base image.

*Bron: blogpost 'Application Layering questions? I got answers. Graphical cheat sheet included!' (2015-12-01), basvankaam.com.*

## Verwante notities

- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [Framing: keep application layering and application virtualization distinct](app-layering-not-app-virtualization.md)
- [Application virtualisation tops out around 70-80% in practice](app-virtualisation-ceiling-70-80.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Application layering vendor landscape circa 2016](application-layering-vendor-landscape-2016.md)
- [Bas: only ~50-60% of apps can be virtualised](bas-on-virtualisation-coverage-50-60-percent.md)
- [How application layering works: filter drivers merging virtual disks](how-application-layering-works-2.md)
- [MSIX positioned to replace App-V (2019 transition)](msix-replacing-app-v.md)
- [If most VDIs are non-persistent, why aren't more apps virtualised?](non-persistent-vs-app-virtualisation-surprise.md)
- [Layering and virtualization are partners, and the cons are soon forgotten](positie-layering-and-virtualization-coexist.md)
- [VAS Application Virtualization Delivery Flow](vas-application-virtualization-flow.md)
- [Windows apps are 'traditional', not 'legacy'](windows-apps-traditional-not-legacy.md)
