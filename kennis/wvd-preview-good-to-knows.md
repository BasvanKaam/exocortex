---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, azure, preview, fslogix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD preview constraints (2019)

How it worked then, during the WVD preview (April 2019):

- All resources had to sit in the same Azure region, and the only region available was East US 2 (possibly Central US). So testing from Europe meant your VMs lived in the US, with the latency that implies. Final judgement should be based on tests run in or near your own region.
- Hosts (VMs) could only be hosted in Azure. No on-premises VMs, no other clouds. This stayed true at GA too.
- Azure AD was not fully supported yet; you had to sync with an existing on-premises Windows Server Active Directory (via Azure AD Connect, Azure AD Domain Services, or your own AD on separate Azure VMs).
- FSLogix bits were a separate download, not yet part of Win10. You did not need Software Assurance for FSLogix, but you did need SA to run server-OS WVD hosts in Azure.
- Skype for Business (and Teams) were officially not supported on WVD; whether that was preview-only or GA too was unclarified.
- Win10 multi-session required a OneDrive per-machine installation, and carried roughly 10-20% more overhead (user-capacity loss) than its server-OS sibling.
- No Linux RDP client could connect to WVD yet; HTML5 browsers all the way.
- Reverse connect (the tech that removes the need for inbound ports to hosts) did not support UDP at the time.
- Win10 multi-session hosts could be used outside WVD, e.g. on Citrix Cloud, as long as they stayed in Azure.

*Bron: blogpost 'When trying out the Windows Virtual Desktop (today), keep the following in mind' (2019-04-10), basvankaam.com.*

## Verwante notities

- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [WVD App Group rules (2019)](wvd-app-groups-rules-2019.md)
- [Even with managed WVD, the customer still owns the base image](wvd-customer-still-owns-the-base-image.md)
- [WVD hit general availability on September 30, 2019](wvd-ga-date-sept-2019.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
- [WVD is not a click-and-go product](wvd-not-click-and-go.md)
- [On-prem WVD looks off the table, GA by summer 2019](wvd-on-prem-out-of-question-positie.md)
- [Not WVD on-prem, but a pragmatic middle ground](wvd-on-prem-workarounds-positie.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
- [WVD roadmap signals from the 2019 workshop](wvd-roadmap-signals-2019.md)
- [WVD tenant setup gotchas (2019 workshop)](wvd-tenant-setup-gotchas-2019.md)
