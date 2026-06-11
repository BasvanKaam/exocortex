---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [windows-server-2012, dotnet, install, troubleshooting]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Server 2012 .NET 3.5 Feature on Demand install gotcha (how it worked then)

Installing Excalibur on Windows Server 2012 needed .NET 3.5, which is a Feature on Demand: the metadata ships in the OS but the binaries do not, so enabling it tries to reach Windows Update. On an isolated lab with no internet the install fails. Bas's fix was to point DISM at the installation media:

`dism /online /enable-feature /featurename:NetFX3 /all /Source:d:\sources\sxs /LimitAccess`

On Server 2008 R2 the Excalibur installer pulled .NET 3.5 in automatically. Dated specifics, but the general lesson (Feature on Demand needs a source on air-gapped boxes) recurs.

*Bron: blogpost 'Project Avalon... Excalibur! Part two' (2013-04-08), basvankaam.com.*

## Verwante notities

- [Early bullish take on Excalibur: impressive, simplified, the right direction](excalibur-impressed-early-take.md)
- [Excalibur merges XenApp and XenDesktop onto FMA](excalibur-merges-xenapp-xendesktop-fma.md)
- [Forcing Microsoft Security Essentials onto Server 2012 (home lab)](mse-on-server-2012-workaround.md)
- [Inspecting prerequisites up front saves the whole deployment](prerequisites-discipline-saves-time.md)
- [XenApp folded into the FMA: the Excalibur / XenDesktop 7.0 moment](xenapp-joins-fma-excalibur-2013.md)
