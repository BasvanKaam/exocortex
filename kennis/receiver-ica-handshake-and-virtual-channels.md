---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-receiver, ica-handshake, virtual-channels, hdx, thinwire]
layer: reference
bron: inside-citrix-fma
---

# Receiver communications, ICA handshake and virtual channels

Citrix Receiver connects to services like XenApp, XenDesktop, XenMobile App Controller, NetScaler Access Gateway and StoreFront. Receiver sits idle during authentication and enumeration (you don't really need Receiver for those), but plays a leading role launching a published desktop/app and establishing the secure connection, channeling the ICA/HDX traffic between client and server.

FMA fact: HDX is not a replacement for the ICA protocol. It is a set of capabilities/technologies offering a high-definition user experience, built on top of the ICA remoting protocol.

Once a resource is launched, the ICA handshake takes place: the client (Receiver) and server (VDA) exchange information on the virtual channels the client supports, so the server knows what to use.

Much client-server communication goes over virtual channels (max 32 total). Each channel has a client-side virtual driver (part of Receiver) talking to a server-side application (part of the VDA). Virtual channels are used for bigger features like client drive mapping, smart cards, clipboard, printing, audio and video. New channels arrive with new versions/Feature Packs (e.g. Framehawk and ThinWire Plus in Feature Pack 3 for XenDesktop 7.6, with Receiver 4.3).

FMA fact: ThinWire is not new; it is a core component of the ICA virtual display channel stack (for over twenty years). The latest addition was rebranded ThinWire Plus.
