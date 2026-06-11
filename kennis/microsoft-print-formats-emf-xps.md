---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, emf, xps, gdi, wpf]
layer: reference
bron: inside-citrix-fma
---

# Microsoft print file formats: EMF vs XPS

Microsoft supports two print file formats: EMF (Enhanced MetaFile) and XPS (XML Paper Specification, often described as Microsoft's less-compatible version of PDF). A print file format refers to the type of print output an application produces and how the print subsystem routes and renders it.

Up to Windows XP / Server 2003, EMF was all that existed, so many applications still depend on it; it remains widely used, perhaps the most. XPS arrived with Windows Vista / Server 2008 and is supported in Windows 7/8/10 and Server 2012/2016. The application's coding determines the format: Win32 GDI applications (C-based framework) use EMF and rely on the Graphics Device Interface; WPF (Windows Presentation Foundation) applications and Win32 XPS applications use the XPS format.

Differences: XPS zips/compresses print data; EMF uses no compression. EMF redraws each image even if reused; XPS can reference a single image multiple times, so EMF print jobs are bigger. XPS suits graphic-rich documents; EMF is perceived as 'faster' because printing can begin after the first page is spooled, whereas XPS waits for all pages.

For XPS to be used, both the print driver (drivers are EMF- or XPS-specific) and the physical device must support XPS (GDI/EMF is the standard). Otherwise an XPS file printed to a GDI device is converted to EMF via the XPS to GDI Conversion Module; conversely EMF output to an XPS device is converted via the GDI to XPS conversion component. The XPS spool markup is compatible with XAML in WPF, so XPS documents render natively in WPF without data/fidelity loss.

## Verwante notities

- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [EMF vs XPS print file formats](emf-vs-xps-print-formats.md)
- [Print driver versions and Print Driver Isolation](print-driver-history-and-modes.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
- [EMF vs XPS print file formats](windows-print-emf-vs-xps.md)
