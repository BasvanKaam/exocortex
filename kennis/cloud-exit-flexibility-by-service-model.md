---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [cloud-exit, iaas, saas, paas, serverless, vendor-lock-in]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Exit flexibility depends on the cloud service model (IaaS/SaaS/PaaS)

Bas's rule of thumb: the closer you are to Infrastructure as a Service (IaaS), the more freedom and control you have, and the easier an exit is. In IaaS you control the operating system, applications and data, so you can move the environment to another provider or back on-premises relatively easily, being less dependent on the provider's cloud-native features. Note: providers do not support each other's VMs (you cannot 'pick up' an Azure VM and drop it on AWS), but migration tools can help - cloud-to-cloud is possible, cloud-to-on-prem (and vice versa) almost certainly is.

With SaaS (e.g. Microsoft 365) you have considerably less control - the provider manages almost everything, so switching is more complex. You depend on the provider's data-export options and may face complex data migration to fit a new system, so think carefully about how to transfer data and functionality.

Cloud-native solutions like PaaS and serverless are often heavily integrated with provider-specific technologies and services, leading to vendor lock-in; an exit can be complex and costly because you often have to adapt or partly rebuild applications. Still, their benefits (scalability, fast implementation) can offset the lock-in risk for some organisations. An effective exit strategy accounts for the different models and the degree of dependency.

## Verwante notities

- [Cloud delivery models: IaaS, PaaS, SaaS and DaaS](cloud-delivery-models-iaas-paas-saas-daas.md)
- [Key Takeaways - cloud exit strategy (Chapter 12)](cloud-exit-key-takeaways.md)
- [Bas's checklist of points of attention for a cloud exit](cloud-exit-points-of-attention.md)
- [A cloud exit strategy is insurance you hope not to need](cloud-exit-strategy-as-insurance.md)
- [Cloud Exit Strategy (start with the exit)](cloud-exit-strategy-cheat-sheet-idea.md)
- [Cloud Exit Strategy: What to Plan For](cloud-exit-strategy-checklist.md)
- [Why have a cloud exit strategy - the exit comes before onboarding](cloud-exit-strategy-rationale.md)
- [Cloud-Native: Designed for the Cloud from the Start](cloud-native-definition.md)
- [No real standards across cloud providers; identical services, different names](cloud-providers-no-standards-naming.md)
- [Opdracht 10: Exit Strategy (XYZ-Care)](exit-strategy-assignment-xyz-care.md)
- [No universal Cloud standard, and the vendor lock-in problem](no-universal-cloud-standard-vendor-lock-in.md)
- [Plan the Exit Before You Commit](plan-the-exit-before-you-commit.md)
