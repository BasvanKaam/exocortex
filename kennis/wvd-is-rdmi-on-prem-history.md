---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, rdmi, rds, reverse-connect, history]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD is what used to be RDMI

WVD's architecture descends from RDMI (Remote Desktop Modern Infrastructure). As originally positioned, RDMI did allow hosts/VMs to live on-premises, something Microsoft explained in presentations and videos. The reverse-connect/proxy approach (no inbound ports to hosts) was introduced with RDMI as well. Architecturally there was nothing stopping Microsoft from letting on-premises hosts connect, which is why on-prem WVD kept being asked for, but in 2019 hosts were Azure-only.

*Bron: blogpost 'Combine WVD, IaaS RDS, on-prem RDS to scale, protect & migrate' (2019-04-29), basvankaam.com.*

## Verwante notities

- [Azure building blocks to extend, protect and migrate RDS/WVD](azure-services-for-rds-wvd-extend-migrate.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [From Terminal Services to AVD - The Multi-User History](history-terminal-services-to-avd.md)
- [Prediction: a multi-user version of Windows 10 is coming](prediction-multi-session-windows-10.md)
- [How Microsoft RDP descended from Citrix's ICA](rdp-descended-from-citrix-ica.md)
- [How Windows 10 multi-session came to light (2018)](windows-10-multi-session-origins-2018.md)
- [Windows Server 2019 at announcement: LTSC/SAC, RDSH question, RDmi](windows-server-2019-ltsc-sac-rdmi.md)
- [On-prem WVD looks off the table, GA by summer 2019](wvd-on-prem-out-of-question-positie.md)
- [Not WVD on-prem, but a pragmatic middle ground](wvd-on-prem-workarounds-positie.md)
- [WVD user connection flow and Reverse Connect](wvd-user-connection-flow-and-reverse-connect.md)
