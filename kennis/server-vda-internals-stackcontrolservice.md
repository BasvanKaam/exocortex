---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, vda, scservice64, stackcontrolservice, broker, termsrv, ica-stack, hdx]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Server VDA internals: StackControlService bridges Broker Agent and ICA stack

How it worked then: there is no PortICA service in a Server VDA, it doesn't exist. During install, the Server VDA registers the Broker Agent Service (direct comms to the Delivery Controller), then installs the multi-user ICA stack which becomes part of Termsrv, creating the ICA stack listener (kernel mode) awaiting connections. It also installs the Citrix Stack Control Service (display name), a.k.a. SCService64, which acts as an interface between BrokerAgent.exe (new FMA) and the ICA stack in Termsrv, mapping a direct COM interface between the two. So SCService64 takes on some responsibilities similar to the PortICA service in a Desktop VDA. The ICA stack itself changed very little under the FMA; its biggest change is the communication interface, now the Broker Agent. The Server VDA extends Microsoft's RDS protocol with the HDX feature set, and is much more lightweight than older XA/ICA installs (though still ~300MB). For troubleshooting these services, use Scout (installed with the Delivery Controller by default).

*Bron: blogpost 'An in-depth look at the Citrix FMA Server VDA… The one that (almost) got away!' (2015-12-16), basvankaam.com.*

## Verwante notities

- [Check FMA service health with PowerShell, not just Director](check-fma-services-with-powershell.md)
- [FMA Server VDA vs Desktop VDA: multi-session and direct controller comms](fma-server-vda-vs-desktop-vda.md)
- [The PortICA service (PicaSvc2.exe) and why it's excluded from default traces](portica-picasvc2-ica-service-role.md)
- [The Server VDA is the component everyone overlooked](positie-server-vda-overlooked.md)
- [Server VDA internals: Broker Agent, ICA stack, StackControlService](server-vda-internals-fma.md)
- [Single-user vs multi-user ICA stack (PortICA) and what it unlocks](single-vs-multi-user-ica-stack.md)
