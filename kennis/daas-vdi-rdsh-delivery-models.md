---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [euc, daas, vdi, rdsh, wvd, cloud]
layer: reference
gedateerd: ja
bron: cgit
---

# DaaS vs VDI vs RDSH delivery models

Three ways to deliver desktops and applications, distinguished by who runs the control plane and where the workloads live.

- **VDI (desktop):** one OS per user. Can run on-prem and in cloud.
- **RDSH (server):** multiple users share a server OS session. Can run on-prem and in cloud.
- **DaaS (desktop and server):** the management/control plane is delivered as a cloud service; workloads can still sit on-prem or in cloud.

Key distinction in the 2019/WVD era: WVD (Windows 10 multi-session, Microsoft) is **Azure only**. Several vendors put their control plane in Azure (sometimes AWS US) while letting the actual workloads run on Azure, other clouds, or on-premises.

Underlying delivery is still based on the Microsoft RDP protocol, single- and multi-user, with HTML5 browser support, SSO/MFA/conditional access, image management and high automation.

*Bron: Salomon-IT '5 alternatieven' (CGIT Event).*

## Verwante notities

- [CloudJumper portfolio: CWMS, CW for Azure, and WVD integration](cloudjumper-portfolio-cwms-cw-for-azure-wvd.md)
- [RDSH vs VDI vs DaaS vs WVD: Single-User and Multi-User Explained](rdsh-vdi-daas-wvd-explained.md)
- [Workspot's cloud-born portfolio: Desktop/Workstation/App/DR Cloud](workspot-four-product-portfolio.md)
