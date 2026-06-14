---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, emf, xps, gdi, spooler, windows]
layer: reference
bron: inside-citrix-fma
---

# EMF vs XPS print file formats

Microsoft supports two print file formats: EMF and XPS.

EMF (Enhanced MetaFile) is the legacy GDI path used by Win32 GDI applications (a C-based framework). Its output is first rendered by the GDI (Graphics Device Interface) before going to the spooler. EMF data is not compressed, and each image must be redrawn every time it is used, so EMF jobs are larger. EMF was the only option up to Windows XP / Server 2003 (EMF development ended there), so a huge install base of apps still depended on it. EMF is perceived as 'faster' because printing can start after the first page spools.

XPS (XML Paper Specification) arrived with Windows Vista / Server 2008 and is used by WPF (Windows Presentation Foundation) and Win32 XPS applications. XPS compresses by zipping print data and can reference a single image multiple times (handy for logos and watermarks). XPS waits for all pages before printing, but is better for graphics-rich documents. To use XPS, both the print device and the print driver must support it; otherwise it falls back to EMF. If an XPS file is printed to a GDI-only device, it is converted back to EMF via the XPS-to-GDI conversion module. The way an application is coded/compiled determines which format it uses.

High-level spooling: the spooler service receives output, the print driver renders the metafile into raw data the device can read (the actual print job), and the spooler sends it to the device. Spooling locally uses local CPU/memory with no network traffic; spooling remotely on a print server uses remote resources and generates extra XenApp-to-print-server network traffic.

*Bron: blogpost 'The ultimate Citrix printing internals cheat sheet - version 2.0' (2017-08-28), basvankaam.com. Aanvullend: Inside Citrix - the FlexCast Management Architecture.*
