---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vda, hsd, xendesktop, rds]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Server VDI vs Hosted Shared Desktop in XenDesktop 7

How it worked then (XenDesktop 7, 2014): **Server VDI** delivers a desktop from a server OS to a single user, one-to-one. It existed since XenDesktop 5.6 and was primarily aimed at service providers wanting true one-to-one cloud VDI while bypassing Microsoft's client-OS licensing restrictions, though it could be used in your own datacenter too.

Key differences versus a Hosted Shared Desktop (HSD) assigned to one user:
- HSD requires the RDS (Terminal Services) role plus a VDA, because it is a multi-user architecture. Server VDI just needs a **client VDA installed with the `/servervdi` switch** (`XenDesktopVdaSetup.exe /quiet /servervdi`), which overrides the installer's default block on a desktop-OS VDA on a server OS. Less overhead.
- HSD can publish/host applications; Server VDI cannot.
- Server VDI requires a XenDesktop license (it is XenDesktop-only) plus a Windows Server CAL. HSD additionally needs a Windows Server RDS CAL plus a XenApp/XenDesktop license.

Server VDI is NOT a cheaper solution; in some cases it is simply the only legal way to deliver one-to-one VDI from the cloud.

*Bron: blogpost 'XenDesktop Single User Server VDI' (2014-01-06), basvankaam.com.*

## Verwante notities

- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [FMA Server VDA vs Desktop VDA: multi-session and direct controller comms](fma-server-vda-vs-desktop-vda.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
- [Server VDI is an underrated, overlooked feature](server-vdi-underrated.md)
- [Features Server VDI cannot do](server-vdi-unsupported-features.md)
- [Single-User vs Multi-User VDI/DaaS](single-user-vs-multi-user-vdi-daas.md)
- [VDI vs RDS vs DaaS, the core distinction](vdi-rds-daas-distinction.md)
- [Bas: the direction is already clear, enough has been said](win10-multiuser-direction-is-clear-2018.md)
