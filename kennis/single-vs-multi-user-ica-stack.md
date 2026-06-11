---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [ica-stack, portica, vda, usb-redirection, hdx]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Single-user vs multi-user ICA stack (PortICA) and what it unlocks

How it worked then (XenDesktop 7): the two VDAs differ at their core in the underlying ICA stack.

- **Client VDA** uses a **single-user ICA stack**, historically called **PortICA**. One user/session at a time, connecting to the machine's console session (like GoToMyPC). It supports extra HDX features unavailable on the multi-user stack, notably **Aero** and the **Generic USB virtual channel** (raw USB redirection) for devices that lack an optimized virtual channel. Server VDI uses this client VDA.
- **Server VDA** uses the **multi-user ICA stack**, same as classic XenApp, allowing many users on one HSD or hosted apps simultaneously. It just has a different UI to fit the FMA infrastructure.

Practical consequence: if a USB device has no optimized virtual channel and its software cannot run on a client OS, Server VDI (single-user stack, with Generic USB redirection) can be the answer where XenApp/HSD would fail. XenApp does NOT offer the Generic USB virtual channel; XenDesktop does.

*Bron: blogpost 'XenDesktop Single User Server VDI' (2014-01-06), basvankaam.com.*

## Verwante notities

- [ICA connection renamed HDX connection (terminology shift, 2013)](ica-connection-becomes-hdx-connection.md)
- [The PortICA service (PicaSvc2.exe) and why it's excluded from default traces](portica-picasvc2-ica-service-role.md)
- [Server VDA internals: Broker Agent, ICA stack, StackControlService](server-vda-internals-fma.md)
- [Server VDA internals: StackControlService bridges Broker Agent and ICA stack](server-vda-internals-stackcontrolservice.md)
