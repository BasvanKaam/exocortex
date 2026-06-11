---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [microsoft, licensing, vda, rds, vdi, software-assurance]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Microsoft VDA vs RDS licensing for Citrix

How the Microsoft side worked circa 2016 (the part that confuses people most).

**The clean rule of thumb:** Microsoft RDS licenses (CALs, per user or device) are needed with Citrix XenApp, not XenDesktop. Microsoft VDA (Virtual Desktop Access) licenses are needed with Citrix XenDesktop (VDI), not XenApp. XenApp runs on top of Microsoft RDS (former Terminal Services), so it needs RDS CALs.

**VDA:** required for each device accessing a Windows *desktop* OS VM (VDI only). ~$100/year per device. Devices covered by Microsoft Software Assurance (SA) or Windows Intune get VDA included automatically; non-Windows thin clients still need separate VDA licenses. Roaming rights: a user with a corporate VDA-licensed device may use their home PC to reach a corporate VM under the same VDA, but bringing a personal device into the corporate domain needs its own license.

**CDL (Companion Device License):** lets one user reach a Windows desktop OS VM from up to four devices (iOS/Android tablets, BYOD). Extra charge, not part of SA. VDA still required underneath.

**SA/VDA per user vs per device:** per-device is more restrictive (roaming limits, may need CDLs); per-user removes those limits, allowing access from all the user's devices.

If you access a Windows desktop OS VM from a physical PC (not a server), no VDA needed, and VDA never applies to XenApp.

*Bron: blogpost 'Citrix licensing (and Microsoft) demystified? I need your help!' (2016-04-18), basvankaam.com.*

## Verwante notities

- [Microsoft CDL (Companion Desktop License)](microsoft-cdl-companion-device-license.md)
- [Microsoft RDS CALs and the XenApp vs XenDesktop split](microsoft-rds-cals-with-xenapp.md)
- [Microsoft VDA licenses and Software Assurance](microsoft-vda-license-software-assurance.md)
- [Positie: the cloud blocker is Microsoft licensing, not the product](positie-blame-microsoft-licensing-not-citrix.md)
- [Positie: the Citrix XD7-on-Azure design guide was misleading marketing](positie-citrix-azure-design-guide-confusing-2013.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
- [How the Citrix license server allocates user/device licenses](user-device-license-server-allocation.md)
- [VDA license rules and Microsoft licensing nuances](vda-license-rules-microsoft-licensing.md)
- [Windows server/desktop OS licensing and App-V (MDOP)](windows-server-desktop-os-licensing-mdop.md)
- [WVD introduced multi-user Windows 10 and a license-based entitlement model](wvd-win10-multiuser-and-licensing.md)
