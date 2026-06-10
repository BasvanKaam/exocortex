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

## Verwante notities

- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [Delivery Controller as the heart of the FMA](delivery-controller-is-heart-of-fma.md)
- [The evolution of the FlexCast Management Architecture](evolution-of-the-fma.md)
- [The eighteen Broker Service Site services (distributed housekeeping)](fma-broker-eighteen-site-services.md)
- [The four most prominent FMA core services](fma-four-prominent-core-services.md)
- [Remaining FMA services: Logging, Delegated Admin, AD Identity, Host, and more](fma-remaining-core-services.md)
- [FMA services: Network Service account and service isolation](fma-services-network-account-and-isolation.md)
- [The nine main FMA components and the XenDesktop Site definition](nine-main-fma-components.md)
- [Using PowerShell to check FMA service states](powershell-fma-service-checks.md)
- [Service logging in XenDesktop (command-line vs Scout)](xendesktop-service-logging.md)
