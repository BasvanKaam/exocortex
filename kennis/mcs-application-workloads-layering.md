---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, app-v, application-layering, containerisation, base-image]
layer: rich
bron: inside-citrix-fma
---

# Bas on MCS, workloads and the case for application layering

Bas's view: "virtualising 100% of your application workload is not going to happen anytime soon." Even when much is virtualised with App-V, applications may be pre-cached, so you still potentially need to 'break open' the base image to update or patch them. The same applies when applications or plug-ins are installed in the base image.

He paints the pain: imagine managing 4+ different base images (master VMs), each with an intensive maintenance cycle driven by home-made applications needing weekly updates. Every week each image needs a new snapshot copied down to all participating datastores, taking up CPU, causing IO peaks and network resource usage. A time-consuming process depending on the number and size of images and datastores.

His FMA fact / takeaway: application layering and containerisation can help overcome most of these application-related issues today, but general adoption of these technologies will still take time. When application virtualisation is not an option, consider application layering as an alternative to installing into the base image.

## Bron-citaten (NL, verbatim)

> As we all know, virtualising 100% of your application workload is not going to happen anytime soon.

## Verwante notities

- [Application delivery: layering vs virtualisation, and AppDisks](application-delivery-layering-vs-virtualisation.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Bas: only ~50-60% of apps can be virtualised](bas-on-virtualisation-coverage-50-60-percent.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [Citrix AppDisks: application layering for golden images](citrix-appdisks-application-layering.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
- [Machine Creation Services essentials](machine-creation-services-essentials.md)
- [Why MCS image updates matter: every master VM is re-copied to every datastore](mcs-image-update-repeats-full-copy.md)
- [Microsoft App-V components and licensing with Citrix](microsoft-app-v-with-citrix.md)
