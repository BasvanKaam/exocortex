---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [vdi, rdsh, daas, wvd, euc, multi-session, citrix, vmware]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# RDSH vs VDI vs DaaS vs WVD: Single-User and Multi-User Explained

A conceptual primer aimed at less technical sales people, written to clear up recurring confusion.

## RDSH (Remote Desktop Session Host)
A role installed on a Microsoft Server OS (e.g. Server 2016/2019); it does not exist on a Windows desktop OS like Windows 10. It lets one application or desktop be shared and used by many people at the same time. This is Multi-User (many-to-one), a concept that has existed 20+ years.

## VDI (Virtual Desktop Infrastructure)
Virtual machines running a desktop OS (usually Windows 10), each assigned one-to-one to a user. Every user works on their own VM. This is Single-User and has existed around 10 years.

## DaaS (Desktop as a Service)
Conceptually equal to VDI (the user works on their own one-to-one desktop), but the technology behind it is usually based on a Server OS (many-to-one), made to feel single-user. This stems from Microsoft desktop-OS licensing, which historically did not allow offering a desktop OS from a shared cloud environment (never a technical problem, a licensing one). Today, under conditions, it is allowed, so DaaS can be implemented in different ways. Conceptually single-user; technically either single- or multi-user.

## WVD (Windows Virtual Desktop)
A new Azure-only Microsoft proposition. The key point: WVD offers a Windows 10 Enterprise Multi-Session image that (under conditions) other DaaS providers may also use. Windows 10 Enterprise Multi-Session is conceptually like RDSH (many-to-one), but the essential difference is that it is a desktop OS shared by multiple simultaneous users, not a server OS.

## Third parties
Citrix (Virtual Apps and Desktops, formerly XenApp/XenDesktop) and VMware Horizon are built on exactly the same underlying Microsoft RDSH technology. They put their own 'shell' over it and add functionality; that added layer is essentially what you pay extra for.

## On-premises vs Cloud
RDSH and VDI can both be built on-premises and in the cloud; the OS type and delivery mechanism depend on several factors. DaaS is cloud-only. Which cloud depends on the chosen solution (Citrix, VMware, CloudJumper, Workspot each have their own). To use the Windows 10 Enterprise Multi-Session image as part of WVD you are tied to Azure, but you remain free to choose your DaaS provider.

*Bron: Salomon-IT 'Een technisch sales verhaal - deel 1 VDI, RDSH etc' (CGIT Blogs).*

## Verwante notities

- [Citrix Cloud / Essentials commercial reality vs the cloud promise](citrix-cloud-essentials-commercial-reality-2017.md)
- [DaaS vs VDI vs RDSH delivery models](daas-vdi-rdsh-delivery-models.md)
- [The Digital Workspace Is More Complex Than People Make It Look](digital-workspace-is-more-complex-than-it-looks.md)
- [How Bas teaches the five essential cloud characteristics](five-essential-cloud-characteristics-teaching.md)
- [From Terminal Services to AVD - The Multi-User History](history-terminal-services-to-avd.md)
- [Baseline Criteria for Modern App and Desktop Delivery (anno 2020)](modern-workplace-delivery-baseline-2020.md)
- [There is no single right way to deliver apps and desktops](no-single-right-way-to-deliver-apps-desktops.md)
- [Single-User vs Multi-User VDI/DaaS](single-user-vs-multi-user-vdi-daas.md)
- [How Windows 10 multi-session came to light (2018)](windows-10-multi-session-origins-2018.md)
- [From RDMI to Windows 10 multi-user: how WVD came to be](wvd-history-rdmi-to-windows-10-multi-user.md)
