---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, app-groups, host-pool]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD App Group rules (2019)

How it worked then for hostpools and App Groups:

- Only one Desktop App Group, but any number of RemoteApp App Groups, per hostpool.
- A user cannot be assigned to both a Desktop App Group and a RemoteApp App Group within the same hostpool.
- Users can be assigned to multiple RemoteApp App Groups.
- All machines within a hostpool should be provisioned from the same image.
- Creating a separate RemoteApp App Group alongside an existing Desktop App Group meant a new/additional VM was needed.
- Load balancing is configured at control-plane level.
- Microsoft flagged that several of these constraints were being worked on.

*Bron: blogpost '49 facts listed - What I picked up during a WVD Solution Design Workshop' (2019-05-13), basvankaam.com.*

## Verwante notities

- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [WVD Spring (ARM) release: Workspaces vs Fall Tenants in NMW](nmw-spring-update-workspaces-vs-fall-tenants.md)
- [Even with managed WVD, the customer still owns the base image](wvd-customer-still-owns-the-base-image.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [WVD preview constraints (2019)](wvd-preview-good-to-knows.md)
- [WVD tenant setup gotchas (2019 workshop)](wvd-tenant-setup-gotchas-2019.md)
