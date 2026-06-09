---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [virtual-channels, dvc, handshake, virtual-driver, sdk]
layer: reference
bron: inside-citrix-fma
---

# ICA virtual channels: 32 total, 17 reserved by Citrix

Much of the client-server communication in ICA happens through virtual channels, where most ICA/HDX features live. Each virtual channel has a client-side virtual driver (in Receiver) that talks to a server-side application (the VDA). Receiver also offers features that need no virtual channel.

There are 32 virtual channels in total; Citrix reserves 17. The remaining ones are available to third parties and customers (dynamic virtual channels, DVCs). They are used for bigger well-known features needing a direct path: client drive mapping, smart cards, clipboard, printing, audio, video, etc. New virtual channels ship with new versions (e.g. Framehawk and ThinWire Plus came with Feature Pack 2 and 3 for XenDesktop 7.6).

Client session launch (the **handshake**): the client connects to the VDA, passes the virtual channels it supports (Receiver version + VDA version matter), the server obtains a channel handle and optionally queries the client, then closes the channel to free resources.

Client-side virtual drivers live in the registry at `HKEY_LOCAL_MACHINE\SOFTWARE\Citrix\ICA Client\Engine\Configuration\Advanced\Modules\ICA 3.0`; remove entries like clipboard or ClientDrive to disable functionality. As a security best practice Citrix recommends disabling unused virtual channels. You can create your own via the Virtual Channel SDK (VCSDK) or the ICA Client Object (ICO) SDK.
