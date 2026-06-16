---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [daas, vdi, fslogix, azure, modern-workplace, design]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# DaaS / VDI Additions to the Technical Design

Bas notes that when the modern workplace based on Cloud technology is in play, Desktop as a Service (DaaS) is often a primary focus, and you add DaaS-specific (and VDI-general) items to the technical design:

- Availability and access: how users reach their virtual desktops (web portal, RDP, specific client software), network connectivity requirements (VPN or direct), and MFA.
- Management and access rights: setup of access/admin rights, roles and responsibilities for managing user profiles, desktop images, application and configuration management.
- Image management: managing standard images (OS, applications, updates); process for creating, updating and maintaining golden images to roll out to virtual desktops.
- Scalability and elasticity: dynamic scaling up/down of desktops on demand (e.g. Azure Autoscaling); define peak capacity and the minimum always-available level for baseline demand.
- User profiles and personal settings: storing profiles using solutions such as FSLogix or other profile-management tools so users get a consistent experience across devices and sessions.
- Security measures for virtual desktops: antivirus, endpoint security, data encryption, settings to prevent data sharing/leaking between desktops and protect user privacy.
- Monitoring and management: monitoring performance/availability with failure and performance alerts; tools/reports for resource use (CPU, RAM, storage), network performance and user experience.
- Cost management and optimisation: tracking costs per user and per desktop, optimising via a tagging strategy, cost centres per subscription, switching off desktops when not in use, budget and alerts, periodic evaluation to prevent cost overruns.

## Verwante notities

- [Autoscaling and the Black Friday Scenario](autoscaling-black-friday-scenario.md)
- [Azure Files: a cloud NAS, plus Azure File Sync for hybrid](azure-files-cloud-nas.md)
- [DaaS Takes Roughly 60% Off Your Hands](daas-takes-60-percent-off-your-hands.md)
- [DaaS versus VDI](daas-vs-vdi.md)
- [Functional Design with Functional Tests](functional-design-and-functional-tests.md)
- [Bas's mini business case: the current-vs-possible mapping table](mini-business-case-current-vs-hybrid-table.md)
- [Parallels RAS (Remote Application Server)](parallels-ras.md)
- [Single-User vs Multi-User VDI/DaaS](single-user-vs-multi-user-vdi-daas.md)
- [Technical/Functional Design as Cloud Blueprint](technical-functional-design-blueprint.md)
- [Windows 365 Cloud PC](windows-365-cloud-pc.md)
