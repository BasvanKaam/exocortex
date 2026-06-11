---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [powershell, studio, xendesktop, automation, fma]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Everything you do in Studio is PowerShell underneath

Durable architectural fact Bas highlights: in the FMA, everything you configure in XenDesktop Studio is actually PowerShell executed in the background. Studio effectively records your manual steps and exposes them as PowerShell you can copy and reuse.

Practical consequence: use the SDK proactively for daily health checks. Status one-liners he recommends: Get-BrokerServiceStatus, Get-SFServiceStatus, Get-HypServiceStatus, Get-ConfigServiceStatus, Get-AcctServiceStatus. The principle, GUI as a thin layer over an automatable API, generalizes well beyond this product.

*Bron: blogpost 'Troubleshooting Citrix XenDesktop & XenApp 7.x ? Read this !' (2014-10-20), basvankaam.com.*

## Verwante notities

- [Check FMA service health with PowerShell, not just Director](check-fma-services-with-powershell.md)
- [Citrix Studio: the central management console](citrix-studio-overview.md)
- [How PowerShell DSC works: authoring, MOF, push and pull](desired-state-configuration-basics.md)
- [Hiding apps (Limit Visibility) vs hiding desktops (PowerShell entitlement filter)](limit-visibility-vs-entitlement.md)
- [Positie: Citrix was inexplicably late adding delegated admin to XenDesktop](positie-citrix-late-with-xendesktop-delegated-admin.md)
- [Using PowerShell to check FMA service states](powershell-fma-service-checks.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [Citrix Studio Configuration sub-nodes](studio-configuration-subnodes.md)
- [XD7 auto-discovers installed apps; App-V replaces Citrix profiling](xd7-app-auto-discovery-and-appv.md)
