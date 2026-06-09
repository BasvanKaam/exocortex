---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, universal-print-server, upd, compression, auto-discovery]
layer: reference
bron: inside-citrix-fma
---

# Citrix Universal Print Server (UPS)

The Universal Print Server (UPS) compresses traffic between a XenApp server and a print server (e.g. when the print server is in a branch office and XenApp in the datacenter) and is optimized for network printing. It works with Linux-based thin clients and tablets, supports both EMF and XPS print formats, and uses the Universal Print Driver (UPD), which can be paired with native drivers for advanced features.

UPS has a server and a client component. The server component (UpsServer) is installed on the print server. The client component is installed on the XenApp/XenDesktop server or VDI VM, available in the standalone VDA installation package. The UPD server component is installed as part of the VDA and includes the Citrix Universal Printer (EMF driver) and Citrix XPS Universal Printer (XPS driver). The UPD client component is installed with Citrix Receiver; it fetches the incoming print stream and forwards it to the UPS local printing subsystem (UPS does not support client-side rendering), where the job is rendered with device-specific drivers. UPS is supported on Windows Server 2016, 2012 R2 and 2008 R2, and requires Microsoft Visual C++ 2013 Runtime (32- and 64-bit).

Flow: after the user clicks print, output (EMF/XPS) goes to the local Windows print subsystem (UPD) on the XenApp server (GDI still intervenes for EMF). Since UPS has no client-side rendering, output is sent to the Citrix UPClient, forwarded to the UPServer (where data can be compressed) instead of straight to the print server spooler, and the Windows print subsystem on the UPS handles rendering/spooling.

UPS is disabled by default; enable it via the 'Universal Print Server Enable' policy. With native drivers paired, it tries the native driver first and falls back to UPD (or can be configured to use UPD directly). Configured network printers leverage UPS automatically via Auto discovery.
