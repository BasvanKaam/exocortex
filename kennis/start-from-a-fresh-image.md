---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, images, best-practice, positie, nerdio]
bron: nerdio-content
---

# Start from a fresh image rather than reusing legacy (Citrix) images

Reusing existing images, especially legacy Citrix images, in Nerdio/AVD often fails for various reasons. My best practice is to start from a fresh image. You can sometimes get a legacy image working by importing it and creating an image object through Nerdio, or by building a new host pool on it, but installing applications can break it and recovery is hit-and-miss. The clean path saves more time than the apparent shortcut of reusing what you already have.

*Bron: Nerdio-content 'Troubleshooting' (Troubeshooting).*

## Verwante notities

- [Application layering toward a zero-app golden image](application-layering-zero-apps-in-golden-image.md)
- [Bas on the 'big, bad image' problem](bas-the-big-bad-base-image.md)
- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Scoping desktop images: what to avoid on an image source VM](nerdio-image-source-vm-scoping-pitfalls.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [App layering that keeps the base image clean is the right model for AVD](positie-app-layering-keeps-the-image-clean.md)
