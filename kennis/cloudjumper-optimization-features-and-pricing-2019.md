---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloudjumper, wvd, cost-optimization, autoscaling, pricing, byol, azure-marketplace]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# CloudJumper optimization features, platform VM, and pricing (2019)

CloudJumper invested in optimizing, not just automating, WVD, VDI and RDSH workloads. Built-in features include Auto Power Down, Wake on Demand, Live Scaling and Workload Scheduling, intended to cut cost and keep the right amount of machines/compute available. During initial setup you configure a 'platform VM' responsible for these extras; with WVD this VM is optional, you only configure it if you want Live Scaling, Workload Scheduling, Wake on Demand, etc.

Commercials (as of 2019): named-user licensing only, starting at 12 dollars per user per month, minimum 10 licenses on an annual basis, support included. Products are available via the Azure Marketplace and the partner channel. Other licenses (Windows 10, Windows Server 2016/2019 as part of WVD, Office 365) fall under BYOL (Bring Your Own License), the approach used by nearly all Marketplace vendors. Additional services include Citrix and RDS migration tools, FSLogix install/config scripts, Azure backup options, OneDrive and Azure Files integration, and an API for third-party extension. Until January 2020, using CWMS in combination with WVD was free (underlying Azure compute still billed to you).

*Bron: CGIT blog 'CloudJumper, onbekend maakt onbemind - deel 2'.*

*Bron: Salomon-IT 'CloudJumper, onbekend maakt onbemind - deel 2' (CGIT Blogs).*

## Verwante notities

- [Cloud cost-optimization levers](cloud-cost-optimization-levers.md)
- [CloudJumper Cloud Workspace Management Suite (WVD GUI)](cloudjumper-cloud-workspace-management-suite.md)
- [CloudJumper portfolio: CWMS, CW for Azure, and WVD integration](cloudjumper-portfolio-cwms-cw-for-azure-wvd.md)
- [FSLogix: the three core technologies after the Microsoft acquisition](fslogix-three-core-technologies.md)
- [Microsoft deliberately leaves WVD management gaps to partners](positie-microsoft-leaves-wvd-management-to-partners-on-purpose.md)
- [Windows Virtual Desktop 2019 launch reference](wvd-2019-launch-reference.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
