---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [on-premises, colocation, managed-service, cloud, hosting, shared-responsibility]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Four Hosting Models - On-Prem, Co-location, Managed, Cloud

Bas lays out a responsibility spectrum across four hosting models:

**On-premises (own datacenter):** everything is the organisation's responsibility — buy, build in, configure and maintain all equipment, plus cooling, power, rack space, network connectivity (often redundant), backup power and physical security. Usually Capex (large initial investment), though renting/leasing can shift it to Opex. Staffing (Opex) is a significant cost since qualified professionals are needed.

**Co-location:** the organisation stays responsible for its own equipment (install, configure, maintain), but the colocation provider supplies cooling, power, rack space, connectivity, backup power and physical security. Costs are typically annual contracts with one-off setup fees plus monthly rack-space and power charges (often on a settlement/nacalculatie basis); bandwidth usually included monthly. Staffing costs stay roughly the same.

**Managed Service:** you no longer buy or build equipment — you rent hardware and software already installed and partly configured. The partner does base config (e.g. the OS) and maintains the OS and underlying hardware, plus the facility items (cooling, power, etc.). Annual contract with setup fees and monthly charges. Required staffing hours drop significantly; patching, data storage and software-level security usually remain the organisation's responsibility (though not always).

**Cloud:** resembles managed services but works differently — resources are shared with other users (you don't notice it). Offers dynamic scalability, pay only for what you use, no upfront costs or long-term contracts (optional), stop anytime and billing stops. Under IaaS/PaaS/SaaS the primary focus stays on managing your own data and apps (patching, storage, software security), while physical infrastructure maintenance falls to the cloud provider.

## Verwante notities

- [Capex and Opex - Pros and Cons](capex-opex-pros-cons.md)
- [Reading the Hosting Spectrum - Capex Falls, Opex Rises](capex-opex-shift-across-hosting-spectrum.md)
- [Chapter 6 Key Takeaways: Capex/Opex, hosting models, business case, VDI/DaaS](chapter-6-key-takeaways-capex-opex-hosting.md)
- [Cloud delivery models: IaaS, PaaS, SaaS and DaaS](cloud-delivery-models-iaas-paas-saas-daas.md)
- [Cloud deployment models (public, private, hybrid, community)](cloud-deployment-models.md)
- [Bas Disagrees With Gartner on Co-location's Demise](gartner-colocation-prediction-disagreement.md)
- [Shared Responsibility Model (Restaurant Analogy)](shared-responsibility-model-restaurant-analogy.md)
