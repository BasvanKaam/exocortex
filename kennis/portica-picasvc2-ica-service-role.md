---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [portica, picasvc2, ica-service, vda, fma, cdf]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The PortICA service (PicaSvc2.exe) and why it's excluded from default traces

How it worked then (XenDesktop 7.x): the PortICA service - renamed PicaSvc2.exe as of 7.x, also called the ICA service - lives on Desktop OS VDAs and handles almost everything happening on the VM except direct communication with the Delivery Controller (which the Desktop service does). On connection it: receives via CGP -> tcpip.sys -> ICA stack, accepts the connection, locks the workstation for authentication, switches the display to remote ICA (Thinwire driver), and exchanges 'pre logon' ticket data via the Desktop service for real credentials.

Key gotcha: by default a CDF trace includes all main FMA services EXCEPT PortICA. When troubleshooting a VDI desktop VM you must manually enable/include the PortICA service in traces and verbose/clear-text logging. You can also exclude any FMA service from tracing by editing its xml config: change <add key="LogToCDF" value="1"/> to value="0".

*Bron: blogpost 'Troubleshooting the XenDesktop FMA - Citrix Scout deep dive, part one' (2015-03-17), basvankaam.com.*

## Verwante notities

- [How CDF tracing works: providers, modules, trace messages](cdf-tracing-providers-modules-messages.md)
- [Check FMA service health with PowerShell, not just Director](check-fma-services-with-powershell.md)
- [Scout 3.0 swapped CDF-Control for Logman.exe (ETW)](citrix-scout-3-cdfcontrol-to-logman.md)
- [Citrix Scout, TaaS and Insight Services as the 2015 troubleshooting chain](citrix-scout-taas-insight-services.md)
- [The FMA's 10 (or 12) primary services and their roles](fma-twelve-services-rundown.md)
- [ICA connection renamed HDX connection (terminology shift, 2013)](ica-connection-becomes-hdx-connection.md)
- [Server VDA internals: Broker Agent, ICA stack, StackControlService](server-vda-internals-fma.md)
- [Server VDA internals: StackControlService bridges Broker Agent and ICA stack](server-vda-internals-stackcontrolservice.md)
- [Single-user vs multi-user ICA stack (PortICA) and what it unlocks](single-vs-multi-user-ica-stack.md)
