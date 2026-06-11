---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, xendesktop, azure, vdi, licensing, cloud, blog-comment, 2013]
bron: basvankaam-blog-comments
---

# Position: client OS VDI from the cloud needs dedicated infra, not multi-tenant Azure

In a 2013 comment thread on "Why you shouldn't deploy XD7 on Azure just yet", Bas stated a clear technical position that went beyond pleasantries, and corrected his own article in the process.

His position, verbatim from the replies:

- Hosting XenApp Hosted Shared Desktops from the cloud (Azure included, as of the 1 July 2013 SAL licenses) is fine: "The license limitations do not apply to the server operating systems, at least not in the same way."
- But on client operating systems: "it is possible to host client operating systems from the cloud, just not from Azure. This is because it's a multi tenant platform, meaning that you'll have to share all underlying resources with other customers (tenants) since you have no control over the underlying hardware, hypervisor included. If you are a Citrix Service Provider and you can offer a dedicated virtual infrastructure including dedicated underlying hardware per tenant (this is the important part), then you would be allowed to host client OSs from the cloud."
- He openly conceded he had missed this nuance in the original article: "that's my bad... I probably should have mentioned this earlier."

He also held his ground against a commenter (David) who read the Citrix design guide differently: "I'm sorry, I can't agree with you. That's not the way they describe it in their design guide," while staying warm ("I deleted the 'misleading' part... I'm still a fan :-)").

Note: this is a 2013 licensing/architecture stance and is almost certainly outdated today (Azure-based client-OS VDI via WVD/AVD later became standard). Kept as a record of his pre-AI position and reasoning style, not as current technical guidance.

*Bron: Bas zijn reactie in de comments op basvankaam.com.*

## Verwante notities

- [Citrix Service Provider (CSP) program](citrix-service-provider-program.md)
- [Client OSes were not allowed on multi-tenant public cloud (2013 licensing)](client-os-not-allowed-multitenant-cloud-2013.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Bas's 2018 reframe: true VDI from the cloud and Microsoft licensing](daas-true-vdi-licensing-evolution.md)
