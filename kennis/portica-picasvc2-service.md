---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [portica, vda, ica-service, cdf, logging]
layer: reference
bron: inside-citrix-fma
---

# PortICA / picaSvc2.exe: the critical VDA ICA service

The PortICA service (renamed picaSvc2.exe as of XenDesktop 7.x, also called the ICA Service) is one of the most important services for a VDI. It 'lives' on desktop-OS-based VMs (VDAs) and handles almost everything on the machine except direct communication with the Delivery Controller (the Desktop service).

During a CDF trace, all main FMA services are included by default except PortICA, which must be enabled by hand. Given its involvement in the initial user connection phase, Bas advises always including PortICA in CDF traces and verbose logging. PortICA logging can be enabled manually (creating a PortICAConfig XML file per CTX118837) or via Scout's GUI (Collect & Upload window, settings icon, swipe the PortICA Service button to On), which automates the same steps. There is no functional difference between the two methods.
