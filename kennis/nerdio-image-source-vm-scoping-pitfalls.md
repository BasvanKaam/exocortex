---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, desktop-images, sysprep, fslogix]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# Scoping desktop images: what to avoid on an image source VM

Reusable guidance Bas teaches when scoping images, beyond the generic image basics already in the brain.

Image type choice drives reusability: a single-user image is one-to-one and cannot later be used for multi-session hosts; a multi-session image can serve multi-session or single-session (personal) hosts. So choose multi-session unless you have a reason not to.

Items to avoid on the image source VM because they break Sysprep or cause issues:
- Domain or Intune join on the source VM - GPOs and Intune policies come into play and can break Sysprep.
- Image-incompatible security products that interrupt Sysprep. Many can be made image-compatible; if not, don't install them on the source VM. (Historically the Zscaler client was not compatible with multi-session VMs.)
- Per-user install applications - install these after host provisioning via UAM or Intune, not on the image.

Keep images light to keep updates and patches fast. dated:true (security-product specifics evolve).

*Bron: Nerdio-content 'NEW_v3.0 Enterprise Training Camp_PRESENTER' (Training).*

## Verwante notities

- [Nerdio Adoption & Management Framework: Five Foundational Elements](nerdio-adoption-management-framework.md)
- [Nerdio Enterprise Optimization Journey (12-step framework)](nerdio-enterprise-optimization-journey.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [Start from a fresh image rather than reusing legacy (Citrix) images](start-from-a-fresh-image.md)
