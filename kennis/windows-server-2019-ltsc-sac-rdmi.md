---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [windows-server-2019, rdsh, ltsc, sac, rdmi, microsoft]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Windows Server 2019 at announcement: LTSC/SAC, RDSH question, RDmi

How it stood in March 2018 (announcement-era facts): Windows Server 2019 focus areas were hybrid cloud (Project Honolulu, Azure integrations), security (Shielded VMs for Linux, encrypted networks, Defender ATP), application platform (containers, WSL, smaller ~5 GB Server Core image, Kubernetes in beta) and HCI. Same licensing model as 2016 but 'highly likely' more expensive (higher CAL costs). Defender ATP, normally in pricier tiers, was being included.

Servicing: an LTSC release (full Desktop Experience plus Server Core/Nano, supported up to 16 years with Premium Assurance, new releases every ~3 years) and a SAC release shipping at the same time, alongside Windows 10 LTSC, Office 2019 and System Center 2019. SAC releases of Windows Server dropped the GUI entirely. Notably, the 2019 preview let you install the Remote Desktop Services / RDSH role but it did not actually work, multiple people tried and failed. Microsoft also announced RDmi (Remote Desktop modern infrastructure) at Ignite 2017: RD backend services running on Azure as a managed .NET Core PaaS, with session hosts and Windows 10 VMs in Azure or on-prem, the precursor to what became Windows Virtual Desktop / Azure Virtual Desktop.

*Bron: blogpost 'Windows Server 2019, but no RDSH? A Multi-User version of Windows 10? What's going on?' (2018-03-26), basvankaam.com.*

## Verwante notities

- [Citrix LTSR vs CR servicing model](citrix-ltsr-vs-cr-servicing.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [Prediction: a multi-user version of Windows 10 is coming](prediction-multi-session-windows-10.md)
- [Bas: the direction is already clear, enough has been said](win10-multiuser-direction-is-clear-2018.md)
- [How Windows 10 multi-session came to light (2018)](windows-10-multi-session-origins-2018.md)
- [Windows Server 2016: native Windows Server containers vs Hyper-V containers](windows-server-2016-container-types.md)
- [Windows 10 servicing branches and deployment rings](windows10-servicing-branches-rings.md)
- [WVD is what used to be RDMI](wvd-is-rdmi-on-prem-history.md)
