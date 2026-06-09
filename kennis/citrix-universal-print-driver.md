---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, upd, emf, xps, pcl, postscript]
layer: reference
bron: inside-citrix-fma
---

# Citrix Universal Print Driver (UPD)

The Universal Print Driver (UPD) is a 'one driver to rule them all' approach, though never quite achievable. Its main limitation is the lack of enhanced printing capabilities, which differ per printer type, hence pairing it with native drivers.

UPD has a client component (holds print drivers, installed with Citrix Receiver) and a server component (installed with the XenApp/XenDesktop VDA, including the Citrix Universal Printer EMF driver and Citrix XPS Universal Printer XPS driver). Both EMF (default) and XPS UPD variants have been enhanced with advanced features like stapling, print draw selection (and existing sorting), and secure PIN printing when available; these are available as of XenDesktop 7.12, and the UPD must be enabled (disabled by default).

FMA fact: enhanced print features work if the native driver exposes them via Microsoft Print Capability technology using standardized Print Schema Keywords in the Print Capabilities XML; non-standard keywords break advanced features under the UPD.

The UPD can be used exclusively (Bas recommends trying this to avoid driver update/conflict issues) or paired with native drivers. By default, if a Windows-native driver isn't available, the system falls back to the UPD. Supported formats: EMF (default), XPS, PCL (PCL5c and PCL4, an HP protocol for basic text/graphics on most HP LaserJets and multifunctionals), Citrix PDF Universal Printer Driver (generates PDFs, enables printing to Receiver for HTML5 and Receiver for Chrome), and PostScript (a language for text and vector graphics, common in low-cost printers and multifunction peripherals).

Key troubleshooting fact: the print driver on the Server OS/VDI VM and the client device must match for printing to succeed; even with the same name, different version numbers mean the drivers are not treated as equal.
