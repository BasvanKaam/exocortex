---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [mdm, enrollment, mobility, concept]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# MDM enrollment binds both the device and the user (durable concept)

A device must first be "known" by the management server (added manually, imported, or auto-discovered) before it can be remotely managed. Then an agent gets installed (usually during enrollment) and the device is bound to an existing user account. Only after that can policies, apps, files and scripts be pushed.

The important conceptual point Bas drew out: enrollment is not just the device getting enrolled, it is the user as well. Resources are applied to groups of users rather than individuals, except during the device enrollment step itself. This device-plus-user binding model is durable and still underpins modern MDM/UEM, even though the specific XenMobile UI is long gone.

*Bron: blogpost 'XenMobile product overview… and It's nice!' (2013-03-12), basvankaam.com.*

## Verwante notities

- [Most companies still get BYOD wrong - policy and management](byod-companies-still-get-it-wrong.md)
- [BYOD has graduated from hype to something you can't ignore](byod-from-hype-to-unavoidable.md)
- [IGEL UMS can manage Windows endpoints, not just IGEL thin clients](igel-ums-manages-windows-endpoints.md)
- [Mobile management acronyms: MDM, MAM, MIM, EMM](mdm-mam-mim-emm-glossary.md)
- [Getting the XenMobile MDM server out of the DMZ was overdue and underdiscussed](mdm-out-of-dmz-relief.md)
- [Use one UEM layer across physical, virtual, on-prem and cloud](one-uem-layer-across-physical-virtual-cloud.md)
- [Workplace Join: registering devices without full domain join](workplace-join-2012r2.md)
- [XenMobile editions: MDM vs Mobile Solutions Bundle (how it worked in 2013)](xenmobile-mdm-editions-and-bundle.md)
- [Worx Home as the XenMobile enrollment and communication hub](xenmobile-worx-home-enrollment.md)
