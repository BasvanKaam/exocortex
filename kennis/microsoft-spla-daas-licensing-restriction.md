---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [microsoft, spla, daas, service-provider, licensing]
layer: reference
bron: inside-citrix-fma
---

# Microsoft SPLA and why true DaaS is restricted

The Microsoft **Services Provider License Agreement (SPLA)** lets service providers and ISVs license eligible Microsoft products monthly under a three-year term to host software services for customers.

For VDI, SPLA is very restrictive: there is no SPLA agreement for multi-tenant/cloud environments when VDI is involved. It is possible only on **dedicated hardware per customer (tenant)** — servers, storage and everything in between must be dedicated, and even with virtualization the physical hosts must be dedicated per customer. This is why true **DaaS** (a desktop Windows OS from the cloud) isn't a viable business case: in roughly 99% of cases XenApp/RDSH technology is used instead. An exception is **Server VDI** (a server OS, mostly Windows Server 2008 R2, used one-to-one), a niche use case. For true cloud-based VDI, customers must provide their own Windows desktop OS licenses — a service provider is not allowed to sell these.
