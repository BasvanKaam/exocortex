---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, emf, xps, gdi, spooler]
layer: reference
bron: inside-citrix-fma
---

# EMF vs XPS print file formats

The two main Microsoft print file formats are EMF and XPS. EMF output is first rendered by the GDI (Graphics Device Interface) before going to the spooler; EMF data is not compressed, and each image must be redrawn every time it is used. XPS was introduced with Windows Vista (EMF development ended with Windows XP / Server 2003), is compressed, and can reference a single image multiple times (handy for logos, watermarks). To use XPS both the print device and the print driver must support it, otherwise it falls back to EMF.

High-level spooling: the spooler service receives output, the print driver renders the metafile into raw data the device can read (the actual print job), and the spooler sends it to the device. Spooling locally uses local CPU/memory with no network traffic; spooling remotely on a print server uses remote resources and generates extra XenApp-to-print-server network traffic.

## Verwante notities

- [Citrix Print Management Service](citrix-print-management-service.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [Citrix Universal Printer (logical print object)](citrix-universal-printer.md)
- [Microsoft print file formats: EMF vs XPS](microsoft-print-formats-emf-xps.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Print driver versions and Print Driver Isolation](print-driver-history-and-modes.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
