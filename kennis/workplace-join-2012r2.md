---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [microsoft, windows-server-2012r2, byod, adfs, mobility]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Workplace Join: registering devices without full domain join

How it worked then (Windows Server 2012 R2, 2013): Workplace Join let admins control access to corporate resources based on application, user, device and location, without fully joining devices to Active Directory. Instead a Workplace-joined device became 'known and trusted'.

Mechanics: the Device Registration Service (DRS), part of the AD Federation Services role in Server 2012 R2, created a device object in AD and issued a certificate representing the device identity. DRS could use a Web Application Proxy so external devices joined over the internet, with single sign-on. At launch only Windows Server 2012 R2 Preview, Windows 8.1 and iOS devices were supported. This is an early form of the 'managed/registered device' concept that later evolved into Azure AD device registration.

*Bron: blogpost 'Mobility based on Windows Server 2012 R2' (2013-10-01), basvankaam.com.*

## Verwante notities

- [Most companies still get BYOD wrong - policy and management](byod-companies-still-get-it-wrong.md)
- [BYOD has graduated from hype to something you can't ignore](byod-from-hype-to-unavoidable.md)
- [2013 mobile management vendor landscape](byod-vendor-landscape-2013.md)
- [MDM enrollment binds both the device and the user (durable concept)](mdm-enrollment-device-then-user.md)
- [Mobile management acronyms: MDM, MAM, MIM, EMM](mdm-mam-mim-emm-glossary.md)
- [SDN via Hyper-V network virtualization (how it worked in 2012 R2)](sdn-network-virtualization-2012r2.md)
- [Work Folders: on-premises file sync as a Dropbox alternative](work-folders-2012r2.md)
