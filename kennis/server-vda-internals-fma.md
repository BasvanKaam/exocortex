---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, vda, fma, ica, rds]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Server VDA internals: Broker Agent, ICA stack, StackControlService

How it worked then (XenDesktop 7 / FMA 2.0, 2014): Unlike XenApp 6.5 and earlier, the FMA Server VDA communicates directly with the Delivery Controller via the Broker Agent (BrokerAgent.exe), the same pattern as the Desktop VDA. Key differences: the Server VDA has no PortICA service. During install it registers the Broker Agent, installs the multi-user ICA stack into Termsrv (the ICA stack listener awaiting connections, in kernel mode), and configures the Citrix Stack Control Service (SCService64.exe), which acts as a COM interface between the Broker Agent and the ICA stack in Termsrv. So SCService64 takes on some of the role PortICA plays in a Desktop VDA. On the Desktop VDA side, the old PortICAsvc.exe (XenDesktop 5.x) was renamed PicaSvc2.exe in XenDesktop 7 and 'just' controls the ICA stack rather than being it. The Server VDA effectively extends Microsoft's RDS protocol with the HDX feature set. It is more lightweight than legacy XA installs (though still ~300 MB) and no longer shares components with the Delivery Controllers, unlike 6.5. Deeply version-specific, kept as a record of how it worked then.

*Bron: blogpost 'XenDesktop 7.x internals continued… The Server VDA in more detail.' (2014-12-15), basvankaam.com.*

## Verwante notities

- [FMA Server VDA vs Desktop VDA: multi-session and direct controller comms](fma-server-vda-vs-desktop-vda.md)
- [The PortICA service (PicaSvc2.exe) and why it's excluded from default traces](portica-picasvc2-ica-service-role.md)
- [The Server VDA is the component everyone overlooked](positie-server-vda-overlooked.md)
- [How Microsoft RDP descended from Citrix's ICA](rdp-descended-from-citrix-ica.md)
- [Server VDA internals: StackControlService bridges Broker Agent and ICA stack](server-vda-internals-stackcontrolservice.md)
- [Single-user vs multi-user ICA stack (PortICA) and what it unlocks](single-vs-multi-user-ica-stack.md)
