---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmm, msp, architecture, azure-paas, multi-tenant]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# NMM architecture: native Azure PaaS deployed into the MSP's own tenant

Nerdio Manager for MSP is built out of native Azure Platform-as-a-Service (PaaS) services deployed from the Azure marketplace into the MSP's own Azure tenant. From that single install, dozens to hundreds of customer accounts/environments/tenants are onboarded and managed from one interface.

Why this matters architecturally:

- Conceptually NMM is an extension layer on top of the native WVD service, adding management capabilities (reporting, monitoring, user management, cost control, role-based access, automation, autoscaling) that also reach other Azure IaaS VMs, plus file storage, networking and identity.
- Because it runs on managed PaaS services that are highly available by nature and managed by Microsoft, the platform is simpler to build, run and enhance.
- It is NOT a shared, hosted management plane. Each MSP gets true multi-tenancy while retaining full control of their own tenant: data, networking, identity, and choice of where metadata is stored and who can access it. No infrastructure shared with other MSPs. Bas frames this as a strong security and privacy story.
- Same underlying architecture as NMW, so the same rapid update/version cadence applies. An NMM API was flagged as coming for future automation and integration.

Summary: 'best of both worlds' = true multi-tenant reach with single-tenant-style control and privacy.

*Bron: Nerdio-content 'Nerdio Manager for MSP unique and flexible deployment architecture_final' (Blogs).*

## Verwante notities

- [Building an MSP cloud practice rests on three pillars](msp-cloud-practice-three-pillars.md)
- [NME to NMM migration runbook (AVD)](nme-to-nmm-migration-runbook.md)
- [Hardening Nerdio Manager for MSP: the private-endpoint pattern](nmm-hardening-private-endpoint-pattern.md)
- [NMW architecture: PaaS-only deploy, metering-only billing](nmw-paas-architecture-and-billing-model.md)
- [NMW is built for enterprise scale; small shops should look elsewhere in the portfolio](nmw-targets-enterprise-not-small-shops-position.md)
