---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [windows-10, multi-session, rdsh, server-2019, avd-precursor]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How Windows 10 multi-session came to light (2018)

How it unfolded, as documented in August 2018, months before the feature shipped. Speculation about a multi-user Windows 10 took off on 20 March 2018 when the RDSH role appeared to be missing from Windows Server 2019 preview build 17623 (selecting the role via "add roles" would fail). Microsoft clarified within ~24 hours via Jeff Woolsey ("...no, it's not gone") and again on 17 April that RDSH would return; build 17650 restored it, attributing the absence to a bug.

The real signal came separately: a Windows 10 "Enterprise for remote sessions" install option spotted by Tero Alhonen in Redstone 5 insider build 17713 (tweeted 1 Aug 2018). Notes from the time: the feature was expected in the Windows 10 1809 (Redstone) release in October 2018, aimed at making apps remotely available to a relatively small number of users per machine, tied to Microsoft's Office 365 ProPlus support, expected to work with Win32 and UWP apps plus Edge, and (per testing) the session count appeared unlimited rather than the originally rumored cap of 10. This is the genesis of what became Windows 10/11 Enterprise multi-session under Azure Virtual Desktop. Licensing and pricing were unknown at the time.

*Bron: blogpost 'Windows 10 multi-user: facts and speculation' (2018-08-21), basvankaam.com.*

## Verwante notities

- [AVD - The Only Cloud Service That Runs Windows Client Multi-User](avd-windows-client-multi-user.md)
- [Prediction: a multi-user version of Windows 10 is coming](prediction-multi-session-windows-10.md)
- [Bas: the direction is already clear, enough has been said](win10-multiuser-direction-is-clear-2018.md)
- [Windows 10 Multi-User (Azure-only) and ProPlus](windows-10-multi-user-azure-only.md)
- [Windows 7 End of Support and the Windows Virtual Desktop (2019)](windows-7-eol-and-wvd-2019.md)
- [Windows Server 2019 at announcement: LTSC/SAC, RDSH question, RDmi](windows-server-2019-ltsc-sac-rdmi.md)
- [Windows 10 Enterprise multi-session performance debate (Ignite 2019)](wvd-ignite-2019-multisession.md)
- [WVD is what used to be RDMI](wvd-is-rdmi-on-prem-history.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [WVD introduced multi-user Windows 10 and a license-based entitlement model](wvd-win10-multiuser-and-licensing.md)
