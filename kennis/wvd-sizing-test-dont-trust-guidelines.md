---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [wvd, avd, sizing, fslogix, poc, method]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# Size virtual desktops by testing, not by general guidelines

Bas's durable planning rule for virtual desktop projects, stated in his WVD-era interview. When planning a deployment, the things to watch are networking (latency) and keeping applications and data close to users (preferably on Azure). VM and user-profile sizing is tricky.

His core stance: don't depend on general guidelines. Stand up a PoC environment and test. Sizing virtual machines and FSLogix profile containers is application- and workload-specific and will differ per environment and per user type (office, power, typical). Give the use case real thought — single-user, persistent, non-persistent, or multi-user (more efficient use of resources) — because all have pros and cons and there is no silver bullet. Don't forget printing either; offices are far from paperless.

*Bron: Nerdio-content 'AzureCrazy Interview Bas van Kaam' ((root)).*

## Verwante notities

- [Azure cost levers: CSP, right-sizing, promos and Reserved Instances](azure-cost-levers-csp-vm-sizing-ri.md)
- [B-series burstable VMs: the CPU-credit model and when to use them](b-series-burstable-vms-explained.md)
- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [IOPS, latency, and sizing storage for VDI workloads](iops-latency-and-sizing-storage-for-vdi.md)
- [Method: Agree PoC Success Criteria Up Front](method-poc-success-criteria.md)
- [Test GPU VMs, don't decide on price alone](test-dont-trust-pricing-on-gpu-vms.md)
- [Estimating WVD cost for under-100-user environments with the Azure calculator](wvd-azure-calculator-small-environment-method.md)
