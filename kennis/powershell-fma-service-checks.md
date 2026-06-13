---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [powershell, fma-services, troubleshooting, director]
layer: rich
bron: inside-citrix-fma
---

# Using PowerShell to check FMA service states

Bas recommends checking the state of your FMA services with PowerShell rather than the Windows services.msc console, because the `Get-` cmdlets are much more detailed and reliable. If you have one or more central management servers, he suggests creating a personal PowerShell profile that runs basic `Get-` FMA service checks automatically each time you open PowerShell. (The green checkmarks next to Delivery Controllers on the Director dashboard are PowerShell `Get-` commands running in the background.)

Example service-status cmdlets:
- Get-BrokerServiceStatus
- Get-ConfigServiceStatus
- Get-HypServiceStatus
- Get-AcctServiceStatus
- Get-ProvServiceStatus

Both Studio and Director run on top of the PowerShell SDK, and everything in Studio (plus extra tweaks not exposed in the GUI) can be done via PowerShell. In Studio, the minutes value next to each Controller indicates when it last registered with the Central Site database and should always be 0; by default a Controller checks in every 20 seconds via heartbeat, valid (TTL) for another 40 seconds.

## Verwante notities

- [Citrix Studio: the central management console](citrix-studio-overview.md)
- [Director dashboard, Trends view and alerts](director-dashboard-trends-and-alerts.md)
- [FMA service high availability via peer service groups](fma-services-high-availability.md)
- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
- [PowerShell: download the latest release asset from GitHub](powershell-download-latest-github-release.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [Everything you do in Studio is PowerShell underneath](studio-is-powershell-underneath.md)
- [VDA registration and how to verify it](vda-registration-and-verification.md)
- [Service logging in XenDesktop (command-line vs Scout)](xendesktop-service-logging.md)
