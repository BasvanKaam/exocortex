---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, emf, xps, gdi, win32, wpf]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# EMF vs XPS print file formats

How it worked (Windows print internals, 2015). Microsoft supports two print file formats:

- EMF (Enhanced MetaFile): legacy but still the most widely used. Everything up to Windows XP / Server 2003 used it, so a huge number of apps depend on it. Win32 (C-based Windows API) applications use EMF. EMF applies no compression and must redraw each image separately even if reused in the same document. EMF output is usually processed by the GDI (Graphical Device Interface) into a metafile before/with a print driver rendering it.
- XPS (XML Paper Specification): introduced with Windows Vista / Server 2008. WPF (Windows Presentation Foundation) apps use XPS. XPS compresses print data into a .zip and can reference a single image multiple times (efficient for logos/watermarks in large documents). For XPS to actually be used, the app, the print driver and the physical printer must all support it - otherwise it converts back to EMF.

Which format an app uses is determined by how it was written/coded.

*Bron: blogpost 'Citrix printing internals cheat sheet… Part one' (2015-10-27), basvankaam.com.*

## Verwante notities

- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [EMF vs XPS print file formats](emf-vs-xps-print-formats.md)
- [Microsoft print file formats: EMF vs XPS](microsoft-print-formats-emf-xps.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Print spooling and the kernel-mode to user-mode driver history](windows-print-spooling-and-driver-history.md)
