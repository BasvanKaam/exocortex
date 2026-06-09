---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [daas, vdi, virtual-desktop, capex, opex, shared-service-center]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# DaaS versus VDI

DaaS (Desktop as a Service) is one of the best-known ways to deliver a modern cloud workplace, and Bas says it's regularly confused with VDI (Virtual Desktop Infrastructure). VDI is not new — it refers to how we traditionally built virtual infrastructures on physical systems in datacenters.

**Similarities:** both give users access to a virtual desktop environment, applications and data from various devices/locations (you just need a good internet connection); central data storage reduces data-loss risk from stolen/lost devices; admins can push updates and maintenance remotely; both often support multiple OSes like Windows and Linux (note: AVD does NOT support Linux).

**Key differences:**
- *Management:* with VDI the organisation usually manages all components itself (physical systems, storage, networks); with DaaS an external cloud provider does this and offers the 'workplace' as a paid service, often with different 'subscriptions'. An internal IT department can itself act as DaaS provider to its employees (a form of DaaS, possibly on VDI or cloud tech), internally charged back via cost centers — e.g. a Shared Service Center acting as the service provider.
- *Initial costs:* VDI needs large upfront hardware/license investment (high Capex); DaaS uses subscription or pay-as-you-go (low initial, Opex).
- *Scalability:* VDI scaling is hard (order/deliver/install hardware); DaaS scales almost instantly via the provider; DaaS needs a stable internet connection (you always work remotely).
- *Management effort:* VDI is higher (IT manages physical infra AND desktop software); DaaS offloads most of this.
- *Backup/DR:* DaaS often arranges this by default or as a subscription option; with VDI it's the organisation's own responsibility.
- *Data location:* VDI can keep data local (more control, more responsibility for security/compliance); DaaS usually stores in the cloud (good for DR/redundancy, but privacy-law/data-protection challenges) — a hybrid model can bridge this.
- *App management & uptime:* VDI gives full control over installed/configured apps; DaaS depends on the provider, but large DaaS providers often offer higher uptime guarantees via advanced redundant datacenters.

Summary: VDI gives more control and customisation but higher costs and complexity; DaaS gives lower initial costs, ideal for fast scaling without large investment.
