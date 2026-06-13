---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmm, msp, wvd, multi-tenant, architecture]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Why Nerdio built a multi-tenant MSP product on top of split-tenant NMW

Nerdio Manager for WVD (NMW) uses a split-tenant architecture: one dedicated NMW installation deployed via the Azure marketplace into each customer's primary Azure AD tenant. That makes it secure by design and flexible for enterprises (stand up a full WVD environment in 60 minutes or less, onboard existing deployments in minutes, monthly release cadence).

The problem for MSPs: they have dozens or hundreds of clients, so one-installation-per-tenant means installing and maintaining dozens of NMW environments and juggling separate accounts to log into each customer. That doesn't scale.

Nerdio Manager for MSP (NMM) was designed from the ground up to solve this: a multi-tenant WVD + Azure IaaS management solution reusing the proven capabilities of Nerdio for Azure (NFA) and NMW. As an MSP you onboard as many customers as you want and reach all of them after a single login to one management console.

Capabilities span autoscaling (WVD and IaaS), automation, auto-deployment, native Azure integrations, plus user, IaaS VM, security, and Microsoft 365 management. Features called out: networking, backups, disk management, user shadowing, Azure Files, role-based access, and MSIX App Attach.

Key takeaway: NMM is the multi-tenant answer to the same problem NMW solved per-tenant, sharing the same underlying architecture so it can innovate at the same rapid release pace.

*Bron: Nerdio-content 'INTRODUCING - Nerdio Manager for MSP_final' (Blogs).*

## Verwante notities

- [Idea: Turn recurring MSP work into repeatable revenue with Nerdio](idee-nerdio-recurring-work-repeatable-revenue.md)
- [Idea: The self-healing MSP environment](idee-self-healing-msp-environment.md)
- [Building an MSP cloud practice rests on three pillars](msp-cloud-practice-three-pillars.md)
- [NME to NMM migration runbook (AVD)](nme-to-nmm-migration-runbook.md)
