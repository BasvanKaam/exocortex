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

## Verwante notities

- [Citrix Service Provider (CSP) program](citrix-service-provider-program.md)
- [CWC as a near-DaaS workaround for Microsoft desktop-OS licensing](cwc-desktop-os-daas-licensing.md)
- [Why DaaS rarely gives you a real client OS (licensing)](daas-client-os-licensing-restriction.md)
- [Bas's 2018 reframe: true VDI from the cloud and Microsoft licensing](daas-true-vdi-licensing-evolution.md)
- [DaaS versus VDI](daas-vs-vdi.md)
- [Microsoft CDL (Companion Desktop License)](microsoft-cdl-companion-device-license.md)
- [Microsoft RDS CALs and the XenApp vs XenDesktop split](microsoft-rds-cals-with-xenapp.md)
- [Microsoft VDA licenses and Software Assurance](microsoft-vda-license-software-assurance.md)
- [VDA license rules and Microsoft licensing nuances](vda-license-rules-microsoft-licensing.md)
