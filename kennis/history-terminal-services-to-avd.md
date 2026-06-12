---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [history, terminal-services, citrix, rdsh, avd, microsoft]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# From Terminal Services to AVD - The Multi-User History

A piece of history Bas notes is often forgotten: the multi-user technology was bought by Microsoft from Citrix. Originally the technology stack was called **Terminal Services**. In 1998 Microsoft bought the licensing rights from Citrix to use the multi-user technology, leading to **Windows NT 4.0 Terminal Server Edition**, which let multiple users remotely access a Windows server and run applications simultaneously — revolutionary at the time.

Timeline:
- This marked the start of Microsoft's terminal services. Terminal Services featured prominently in Windows 2000, Windows Server 2003 and Windows Server 2008.
- With **Windows Server 2008 R2 (2009)**, Microsoft renamed Terminal Services to **Remote Desktop Services (RDS)** and introduced the Remote Desktop Session Host (RDSH) role, bringing improved user experiences, VDI and better scalability.
- From **2019** Microsoft launched **Windows Virtual Desktop (now Azure Virtual Desktop)**, building on RDS. Though AVD is more advanced, the basic concept of multi-user sessions on a single host is still comparable to old RDSH technology.
- **W365 Cloud PC** is built on the same underlying architecture, though Cloud PCs are single-user machines, always on, a fixed monthly cost, and managed via Intune like a physical PC.

Trivia from Bas: before AVD was named AVD it had other names — WVD (Windows Virtual Desktop) before that, and briefly RDSH/RDmi (Remote Desktop Services Infrastructure). Microsoft's internal project codename was **Cowbell** — American slang for something extra that isn't strictly necessary but makes things nicer or better.

## Bron-citaten (NL, verbatim)

> “Oorspronkelijk werd deze technologie stack Terminal Services genoemd. In 1998 kocht Microsoft de licentierechten van Citrix om de multi-user-technologie te gebruiken.”
>
> gaven ze het project een interne naan, namelijk, Cowbell

## Verwante notities

- [AVD - The Only Cloud Service That Runs Windows Client Multi-User](avd-windows-client-multi-user.md)
- [Citrix origins: from Citrus Systems to WinFrame, and the birth of ICA](citrix-origins-and-ica-birth.md)
- [DaaS provider takes roughly 60% of the management off the IT department](daas-vendor-takes-60-percent-of-management.md)
- [DaaS versus VDI](daas-vs-vdi.md)
- [The origin of Citrix and the ICA protocol](history-of-citrix-and-ica.md)
- [ICA protocol origin and the birth of Microsoft RDP](ica-protocol-origin-and-rdp.md)
- [Bas's reframe: is AVD and/or Windows 365 Cloud PC really DaaS?](is-avd-and-windows-365-really-daas.md)
- [Microsoft RDS CALs and the XenApp vs XenDesktop split](microsoft-rds-cals-with-xenapp.md)
- [Office 365 ProPlus on Remote Desktop Services](o365-proplus-on-rds.md)
- [ProPlus on RDS and shared computer activation](office-365-proplus-on-rds-shared-computer-activation.md)
- [RDSH vs VDI vs DaaS vs WVD: Single-User and Multi-User Explained](rdsh-vdi-daas-wvd-explained.md)
- [Terminal Server licensing and RDP basics (reference)](terminal-server-licensing-and-rdp-basics.md)
- [Windows 10 Multi-User (Azure-only) and ProPlus](windows-10-multi-user-azure-only.md)
- [Windows 365 Cloud PC](windows-365-cloud-pc.md)
- [Windows 7 End of Support and the Windows Virtual Desktop (2019)](windows-7-eol-and-wvd-2019.md)
- [WVD hit general availability on September 30, 2019](wvd-ga-date-sept-2019.md)
- [WVD is what used to be RDMI](wvd-is-rdmi-on-prem-history.md)
