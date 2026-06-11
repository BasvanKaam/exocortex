---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [server-vda, desktop-vda, rdsh, xenapp, scservice64]
layer: rich
bron: inside-citrix-fma
---

# Server VDA vs Desktop VDA: the often-overlooked new component

Bas notes what surprises him: since XenDesktop 7 integrated XenApp, the **Server VDA** is almost never mentioned, even though it was a brand-new component. Never before was it optional to install a lightweight agent onto a XenApp server: it was all or nothing.

The Server VDA was built from the ground up but resembles the old ICA protocol stack of XenApp 6.5 and earlier. Unlike XenApp, the VDA communicates directly with the Delivery Controller via the Broker Agent, like the desktop VDA (PortICA).

Key differences:
- The Server VDA accepts and manages **multiple** user sessions at once (RDSH/XenApp model); the Desktop VDA (PortICA) handles only one ICA session at a time.
- Both communicate directly and exclusively with the Controller and need no access to the Central Site Database or license server.
- The RDSH/XenApp server OS need not match the Controller's OS; multiple OSes per Site are fine.
- There is **no PortICA service** in a Server VDA: it simply does not exist.
- During Server VDA install it registers the Broker Agent Service, installs the multi-user ICA stack (becoming part of Termsrv, creating the ICA stack listener), and installs the **Citrix Stack Control Service** (SCService64.exe). SCService64 acts as an interface between the Broker Agent and the ICA stack in Termsrv via a direct COM interface, taking on some responsibilities similar to PortICA in a Desktop VDA.
- Non-brokered RDP connections are allowed on both; non-brokered ICA connections are allowed on the Server VDA but not on the Desktop VDA (except in HA mode).

The Server VDA is much more simplified and lightweight than earlier XA/ICA installs (though still over 300 MB), consisting only of components needed to host sessions. Bas thanks Mick Glover (his "FMA partner in crime") and Martin Zugec for answering his questions on this chapter.

## Verwante notities

- [Desktop VDA core services: Citrix Desktop Service and Citrix ICA Service](desktop-vda-two-main-services.md)
- [Microsoft RDS CALs and the XenApp vs XenDesktop split](microsoft-rds-cals-with-xenapp.md)
- [PortICA / picaSvc2.exe: the critical VDA ICA service](portica-picasvc2-service.md)
- [The Server VDA is the component everyone overlooked](positie-server-vda-overlooked.md)
- [Single-User vs Multi-User VDI/DaaS](single-user-vs-multi-user-vdi-daas.md)
- [Two VDA types and the single-user vs multi-user ICA stack](two-vda-types-ica-stack-difference.md)
- [VDA install options and supported operating systems](vda-install-options-and-supported-os.md)
- [The VDA: client-side component, services and registration](vda-overview-services-and-registration.md)
- [XenApp folded into the FMA: the Excalibur / XenDesktop 7.0 moment](xenapp-joins-fma-excalibur-2013.md)
