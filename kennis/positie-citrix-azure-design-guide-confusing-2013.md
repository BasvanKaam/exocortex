---
type: positie
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [citrix, azure, critique, documentation]
bron: basvankaam-blog
---

# Positie: the Citrix XD7-on-Azure design guide was misleading marketing

Bas publicly criticised Citrix's XenDesktop 7 on Windows Azure design guide (Aug 2013). His core objection: the guide presents an example deployment with a catalog of five Windows 7 client-OS VDI machines and claims 'Server VDI Workers' are supported, which contradicts Microsoft's rule that client OSes cannot run on multi-tenant Azure. The document also failed to mention License Mobility, Software Assurance, or the service-provider/SAL requirements.

His framing: 'you must admit (or not :-) that the way Citrix introduced XD7's availability on Azure, including the accompanying design document, isn't their best work up to date. It's confusing.' He was careful to attribute it to an over-excited marketing department rather than the product itself. The comment thread (including Citrix's Kurt Moody) became a substantive back-and-forth, which led to the follow-up post idx 24. Notable for showing his willingness to call out a major vendor in public while staying collegial.

*Bron: blogpost 'Why you shouldn't deploy XD7 on Azure just yet.' (2013-08-18), basvankaam.com.*

## Verwante notities

- [Correct build order for an early Azure test lab](azure-classic-test-lab-build-order.md)
- [Azure forced Microsoft's OS and application templates (2013)](azure-os-application-templates-2013.md)
- [Client OSes were not allowed on multi-tenant public cloud (2013 licensing)](client-os-not-allowed-multitenant-cloud-2013.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Microsoft VDA vs RDS licensing for Citrix](microsoft-vda-rds-licensing-for-citrix.md)
- [Positie: the cloud blocker is Microsoft licensing, not the product](positie-blame-microsoft-licensing-not-citrix.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
- [RDS SALs required SPLA / service-provider status (2013)](rds-sals-require-spla-service-provider-2013.md)
- [Summarize the features, spare people the marketing propaganda](skip-the-marketing-propaganda.md)
- [Why true Windows desktop DaaS was blocked by SPLA](splash-spla-no-true-windows-daas.md)
