---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [faas, serverless, azure-functions, aws-lambda, scaling]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# FaaS / Serverless Computing Explained

Function as a Service (FaaS), or serverless computing, runs backend code (functions) without you having to manage systems or applications. The Cloud platform takes over the system logic, so developers can focus entirely on writing and running the application.

Book example: an app where customers upload photos that are automatically resized for a website. Traditionally this needed a server running constantly even if photos arrived only occasionally. With FaaS, a function (a small piece of code) runs only when a customer uploads a photo; it starts automatically, resizes the photo (a few seconds), saves it, then stops. Bas compares it to a motion-sensor light that switches on briefly when you approach and off again by itself. You pay only for the seconds the function is active, maintenance is simplified, and costs are often much lower. If hundreds or thousands of photos suddenly arrive, the backend scales up and down automatically.

Netflix uses this kind of technology (Lambda functions on AWS); Netflix runs its own tech blog on the topic.

Bas notes FaaS is relatively rare in practice, usually less suited to smaller organizations or IT service providers, and even when used you typically don't notice it.

## Verwante notities

- [Autoscaling and the Black Friday Scenario](autoscaling-black-friday-scenario.md)
- [Bas: 'Wegwerp IT' and the Lift-and-Shift Caution](bas-wegwerp-it-and-lift-and-shift.md)
- [Reading the Hosting Spectrum - Capex Falls, Opex Rises](capex-opex-shift-across-hosting-spectrum.md)
- [Cloud-Native: Designed for the Cloud from the Start](cloud-native-definition.md)
- [Cloud service models: SaaS, PaaS, IaaS, DaaS](cloud-service-models-saas-paas-iaas-daas.md)
- [Core cloud building blocks: datacenter, virtualization, APIs, storage, databases, elasticity](core-cloud-components-and-concepts.md)
- [Edge computing and Edge-nodes](edge-computing.md)
- [Google Cloud cost management and optimisation tools](gcp-cost-management-tools.md)
- [Obvious cloud trends (multi-cloud, edge, zero trust, serverless, green)](obvious-cloud-trends-list.md)
