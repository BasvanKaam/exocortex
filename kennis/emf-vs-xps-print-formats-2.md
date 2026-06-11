---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, windows, emf, xps, gdi]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# EMF vs XPS: the two Windows print file formats

How it worked then (2017, Win32-era Windows printing). Microsoft supported two print file formats. EMF (Enhanced MetaFile) is the legacy GDI path used by Win32 GDI applications (C-based framework); it was the only option up to Windows XP / Server 2003, so a huge install base of apps still depended on it. XPS (XML Paper Specification) arrived with Vista / Server 2008 and is used by WPF (Windows Presentation Foundation) and Win32 XPS applications.

Differences: XPS compresses by zipping print data and can reference a single image multiple times; EMF uses no compression and redraws each image even when reused, so EMF jobs are larger. EMF is perceived as 'faster' because printing can start after the first page spools, while XPS waits for all pages. XPS is better for graphics-rich documents. If an XPS file is printed to a GDI-only device, it is converted back to EMF via the XPS-to-GDI conversion module. The way an application is coded/compiled determines which format it uses.

*Bron: blogpost 'The ultimate Citrix printing internals cheat sheet - version 2.0' (2017-08-28), basvankaam.com.*

## Verwante notities

- [EMF vs XPS print file formats](windows-print-emf-vs-xps.md)
