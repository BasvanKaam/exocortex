---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, azure, base-image, migration]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Even with managed WVD, the customer still owns the base image

A key early WVD clarification (Feb 2019): although the Windows Virtual Desktop is a fully managed service for the back-end control-plane components, the base image holding your applications, plug-ins, OS and other software is still something the customer must own and maintain (or have a partner do it). When provisioning WVD machines, knowing the amount and type of Azure storage needed up front smooths the process, and understanding how users behave through the week helps assign proper resources.

How it worked then under early WVD; the 'managed service does not mean managed image' point endures conceptually across what became Azure Virtual Desktop.

*Bron: blogpost 'Transitioning to the Windows Virtual Desktop using Liquidware solutions' (2019-02-25), basvankaam.com.*

## Verwante notities

- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [WVD App Group rules (2019)](wvd-app-groups-rules-2019.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [WVD preview constraints (2019)](wvd-preview-good-to-knows.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
