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
