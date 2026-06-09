---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, universal-printer, upd, logon-performance]
layer: reference
bron: inside-citrix-fma
---

# Citrix Universal Printer (logical print object)

By default, when a user establishes a session on a Citrix server, either no default printers or all client-known printers are mapped into the session. When you enable and configure the Universal Printer instead, it creates a single generic/logical print object at the start of the session, so no printer enumeration occurs, speeding up logon. This is useful when the 'Wait for printer to be created' policy is used or when you need access to multiple local and network printers.

This logical object is virtually mapped to the client's default configured printer (but can be set to any client-known printer). The Citrix Universal Printer is part of the UPD (installed with the XenApp/XenDesktop VDA) and only works with Windows clients; the VDA installs the Citrix Universal Printer (EMF driver) and Citrix XPS Universal Printer (XPS driver), so the Universal Printer uses the UPD as its default driver.
