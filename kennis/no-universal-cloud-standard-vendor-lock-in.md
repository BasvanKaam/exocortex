---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [vendor-lock-in, standards, exit-strategy, kubernetes, azure-arc]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# No universal Cloud standard, and the vendor lock-in problem

Bas notes that although Cloud computing has existed for over 15 years and matured, there is still no universal standard all providers follow. When AWS, the first big public Cloud provider, started, there was hope it would set the standard - but as Azure and Google launched their own services, visible differences emerged in how they design and deliver infrastructure. A simple example: a VM created on Azure cannot simply be moved to AWS or vice versa (it can, but only using third-party migration software).

This lack of standardised processes leads to vendor lock-in: companies that invest in a specific provider become dependent on it, making switching costly and complex, limiting flexibility. Bas draws an interesting lesson - the importance of a Cloud exit strategy. Because provider infrastructure and services are not always interchangeable, organisations must plan how to migrate to another provider or even back to on-premises without major disruption. This demands careful IT architecture design and avoiding proprietary technologies tied to one provider.

The landscape is improving: containers, Kubernetes and Azure Arc offer more flexibility. Containers isolate applications from the underlying infrastructure, easing movement between providers. Kubernetes (open-source) standardises running containerised workloads regardless of provider. Azure Arc lets you use and manage Azure services in on-premises or hybrid environments (also used in Azure Stack HCI, now renamed Azure Local). Open APIs likewise reduce single-provider dependence - but Bas stresses 'open' is the key word (a product-specific API can cause the same challenges) and that this requires specialist knowledge and is not easy.

## Verwante notities

- [Azure Stack HCI (renamed Azure Local): cloud in your own datacenter](azure-stack-hci-azure-local.md)
- [Bas's Cloud 'Cheat Sheets' mapping provider service names](bas-cloud-cheat-sheets.md)
- [Bas deconstructs the cloud promises](bas-deconstructs-the-cloud-promises.md)
- [Bas's War Story: The IaC Dependency Trap](bas-iac-dependency-trap.md)
- [The human factor: loss of control and trust](bas-on-the-human-factor-and-loss-of-control.md)
- [Paper conclusion: Cloud only? Maybe never](bas-paper-conclusion-cloud-only-never.md)
- [Exit flexibility depends on the cloud service model (IaaS/SaaS/PaaS)](cloud-exit-flexibility-by-service-model.md)
- [Why have a cloud exit strategy - the exit comes before onboarding](cloud-exit-strategy-rationale.md)
- [No real standards across cloud providers; identical services, different names](cloud-providers-no-standards-naming.md)
- [Same cloud service, different name per vendor](cloud-service-naming-differs-per-vendor.md)
- [Choosing a CSP: Azure as the Default for Microsoft Shops](csp-platform-choice-azure-default.md)
- [Position: Don't Let MSP Tooling Choices Create Lock-In](position-avoid-msp-tooling-lock-in.md)
- [Have a cloud exit strategy; lock-in and weak portability are real](position-cloud-exit-strategy.md)
- [A Cloud Strategy without a reversibility plan is incomplete](position-cloud-strategy-needs-exit-strategy.md)
- [Think about the cloud exit before you onboard](the-exit-comes-before-onboarding-stance.md)
- [The promises of the Cloud (and Bas's invitation to challenge them)](the-promises-of-the-cloud.md)
