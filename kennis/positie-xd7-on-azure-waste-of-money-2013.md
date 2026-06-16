---
type: positie
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure, xendesktop, positie, licensing]
bron: basvankaam-blog
---

# Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013

In August 2013, shortly after Citrix and Microsoft announced XenDesktop 7 availability on Azure, Bas argued you should not deploy it there yet. His reasoning: licensing limits the deployment to Hosted Shared Desktops only, so you pay full XD7 price and can only use half of what you bought.

His stance, in his words: 'Personally I think it's a waste of money. You buy XenDesktop 7, which we all know isn't cheap, host it on Azure to find out that you can only use half of what you paid for.' His advice was to be patient, run XD7 on-premises for now, or deploy XenApp instead which had great Azure use cases. He also pinned the blame squarely on Microsoft licensing, not on the technology: XD7 was as cloud-ready as it would ever be.

Forward-looking note: he flagged Microsoft's then-secret 'Mohoro' project as a possible future enabler of true cloud VDI with client OSes, expected second half of 2014. (Mohoro later became Azure RemoteApp.)

*Bron: blogpost 'Why you shouldn't deploy XD7 on Azure just yet.' (2013-08-18), basvankaam.com.*

## Verwante notities

- [Immutable names and per-VM RDP endpoints in classic Azure](azure-classic-immutable-names-and-rdp-endpoints.md)
- [Azure forced Microsoft's OS and application templates (2013)](azure-os-application-templates-2013.md)
- [Azure building blocks to extend, protect and migrate RDS/WVD](azure-services-for-rds-wvd-extend-migrate.md)
- [Client OSes were not allowed on multi-tenant public cloud (2013 licensing)](client-os-not-allowed-multitenant-cloud-2013.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Microsoft VDA vs RDS licensing for Citrix](microsoft-vda-rds-licensing-for-citrix.md)
- [Positie: the cloud blocker is Microsoft licensing, not the product](positie-blame-microsoft-licensing-not-citrix.md)
- [Positie: the Citrix XD7-on-Azure design guide was misleading marketing](positie-citrix-azure-design-guide-confusing-2013.md)
- [Server VDI vs Hosted Shared Desktop in XenDesktop 7](server-vdi-vs-hsd.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [XenApp Express: the Citrix/Microsoft replacement for Azure RemoteApp](xenapp-express-replaces-azure-remoteapp.md)
- [XenDesktop 7 editions and licensing models](xendesktop7-editions-and-licensing.md)
