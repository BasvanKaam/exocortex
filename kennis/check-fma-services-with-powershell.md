---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, powershell, director, monitoring, troubleshooting]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Check FMA service health with PowerShell, not just Director

How it worked then: Director/Monitor service alerts tell you THAT a service is wrong and when, but not WHAT is wrong or where to look. PowerShell tells you what is wrong (or points you in the right direction), and Director doesn't even monitor all FMA services by default - PowerShell can. Example status cmdlets: Get-BrokerServiceStatus, Get-ConfigServiceStatus, Get-HypServiceStatus, Get-AcctServiceStatus, Get-ProvServiceStatus.

Practical tips: on a central management server, build a personal PowerShell profile that runs these Get- service checks every time you open PowerShell. Use the PowerShell console built into Citrix Studio (no need to load CTX snap-ins/modules). Both Studio and Director run on top of the PowerShell SDK - anything in Studio can be done in PowerShell and vice versa, and PowerShell exposes extra config options Studio doesn't. (SCOM running these every 2-5 minutes is possible but likely overkill.)

*Bron: blogpost '12 services that make up the Citrix XenDesktop Flex Management Architecture' (2015-03-26), basvankaam.com.*

## Verwante notities

- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [The FMA core services and how they communicate](fma-services-complete-overview.md)
- [FMA services run independently, with separate DB connection strings](fma-services-independent-registry-accounts.md)
- [The FMA's 10 (or 12) primary services and their roles](fma-twelve-services-rundown.md)
- [The PortICA service (PicaSvc2.exe) and why it's excluded from default traces](portica-picasvc2-ica-service-role.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [Server VDA internals: StackControlService bridges Broker Agent and ICA stack](server-vda-internals-stackcontrolservice.md)
- [Everything you do in Studio is PowerShell underneath](studio-is-powershell-underneath.md)
- [Use health-check tooling proactively, not only when things fall apart](use-monitoring-proactively-not-when-it-breaks.md)
