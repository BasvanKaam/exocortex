---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [troubleshooting, logging, scout, fma-services]
layer: reference
bron: inside-citrix-fma
---

# Service logging in XenDesktop (command-line vs Scout)

XenDesktop supports service logging, enabled either from the command-line or through Citrix Scout's GUI (Scout is installed by default on XenDesktop/XenApp Delivery Controllers). Scout cannot log certain services such as the Broker Agent (part of the VDA as of 7.x); enabling logging via the command-line makes all services available. Scout-monitorable services include ADIdentity, Broker, Configuration, Host, Machine Identity and Machine Creation.

Example manual command-line: `Citrix.MachineCreation.SdkWcfEndpoint.exe -LogFile C:\XDLogs\Name.log`

Key services to watch when troubleshooting connectivity: the Delivery Controller's Broker Service log, the VDA's Broker Agent log (CTX117452), and the PortICA service (the ICA Service), which handles nearly everything from an ICA/HDX perspective except direct communication with the Delivery Controller. PortICA logging is not enabled by default on the VDA (CTX118837).
