---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [cloud-pc, windows-365, avd, decision-framework, fslogix, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Cloud PC vs AVD: a four-lens decision framework

Bas's reusable method for choosing between Cloud PC and AVD: break the decision into four categories rather than arguing feature-by-feature. The whole choice comes down to flexibility and how much you need to manage and customize machines, apps, and Azure resources.

The four lenses:
1. **Technical architecture** (control plane, subscriptions, compute, storage, networking, profiles, identity)
2. **IT admin experience** (management portal, OS support, image management, app/update delivery, backup/DR, monitoring, autoscaling)
3. **End-user experience** (connectivity clients, printing/scanning, user self-service)
4. **Licensing and infrastructure costs**

Durable architectural distinctions that survive product renames:
- **Compute/storage/cost model**: Cloud PC is Microsoft-managed, fixed monthly cost, no direct admin access to the VMs; AVD is customer-managed, usage-based, flexible. Autoscaling (and its ~75% peak-cost saving) only exists on AVD because Cloud PC's price is fixed per month.
- **Storage and profiles**: Cloud PC stores the profile natively on C: (no FSLogix), which makes backup harder; AVD uses OS disks + FSLogix (mandatory on pooled), easy to back up.
- **Networking**: customer-managed and flexible on AVD and MEM-managed Cloud PC; Microsoft-managed and non-configurable on self-service Cloud PC.
- **OS**: Cloud PC is single-session Windows 10/11 Enterprise only; AVD also supports multi-session (EVD) and Server.
- **Image management**: AVD supports image-based management; Cloud PC does not, because the VMs are persistent.
- **Self-service**: Cloud PC users get a built-in HTML self-service portal (cloudpc.microsoft.com); AVD has none natively and needs a third-party tool like Nerdio Manager.
- **Identity (2021 state)**: MEM-managed Cloud PC needs Hybrid AD join (no Azure AD DS); self-service is Azure AD join only; AVD requires AD DS.

*Bron: Nerdio-content 'When CPC when AVD' (Blogs).*

## Verwante notities

- [AVD vs Cloud PC is a control-vs-simplicity trade-off keyed to your team's Azure skill](avd-vs-cloud-pc-it-depends-on-team-skill.md)
- [Cloud PC licensing requirements (durable)](cloud-pc-licensing-requirements.md)
- [Cloud PC: MEM-managed vs self-service (durable distinction)](cloud-pc-mem-managed-vs-self-service.md)
- [Bas's reframe: is AVD and/or Windows 365 Cloud PC really DaaS?](is-avd-and-windows-365-really-daas.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-added-value-on-cloud-pc.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [AVD and Cloud PC go hand in hand, pick per use case](positie-avd-en-cloud-pc-gaan-hand-in-hand.md)
- [Windows 365 and AVD Are Complementary, Not Competing](positie-w365-and-avd-coexist.md)
- [Simplicity comes at the cost of flexibility](simplicity-costs-flexibility.md)
- [Windows 365 Cloud PC: What It Is and How It Differs from AVD](w365-cloud-pc-vs-avd-fundamentals.md)
- [Windows 365 Cloud PC - Pros, Cons and Cost Control vs AVD](windows-365-pros-cons.md)
