---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [appstream, app-management, positie, flexapp]
bron: basvankaam-blog
---

# Cloud-native does not fix application management

May 2019. AWS claims AppStream simplifies application management, improves security and reduces costs. Bas's stance: 'I would agree, except for the management part.' His point is that remoting apps (streamed or published) is not new, and AppStream's native model installs apps directly into images with no abstraction between app and OS, so 'New technology, same (management) challenges'. The cloud-native scaling is genuinely useful, but from an app-management view 'not much has changed'. That gap is exactly why FlexApp layering (via AppStream 2.0's Dynamic Apps) matters. He also predicts published/streamed app delivery will be 'one of the main use-cases of WVD, once it's available world-wide'. A consistent Bas theme: be skeptical of 'the cloud solves it' marketing where the underlying management problem persists.

*Bron: blogpost 'AWS launched AppStream 2.0, here's how Liquidware adds some 'magic' on top' (2019-05-08), basvankaam.com.*

## Verwante notities

- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [How AWS AppStream 2.0 streams apps (2019)](appstream-fleets-image-builder.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [Cloud is a potential solution, not a silver bullet](cloud-is-no-silver-bullet.md)
- [Don't be fooled by DaaS marketing](dont-be-fooled-by-daas-marketing-position.md)
- [If most VDIs are non-persistent, why aren't more apps virtualised?](non-persistent-vs-app-virtualisation-surprise.md)
