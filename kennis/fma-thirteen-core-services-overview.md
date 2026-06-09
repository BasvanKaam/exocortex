---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, delivery-controller, core-services, xendesktop, architecture]
layer: reference
bron: inside-citrix-fma
---

# The FlexCast Management Architecture and its thirteen core services

The FMA is the foundation of Citrix's application and desktop virtualisation platforms. It has always been Citrix's next-generation VDI architecture and evolved to also support XenApp/RDSH workloads (the book is at XenDesktop/XenApp 7.8, with new LHC services in 7.12).

The FMA is built around thirteen core services. It evolved from six services in 2010 to thirteen, and is designed using clearly defined standards so new functionality can be added either as new services or built on top of existing ones.

The **Delivery Controller** is often called the heart of the FMA because all thirteen services live on the Delivery Controllers. The Controller only manages and brokers connections to managed and unmanaged VDAs; it hosts no sessions of its own. All ICA/HDX bits and related services reside on the VDA itself. As a best practice deploy two or more Delivery Controllers to avoid a single point of failure.
