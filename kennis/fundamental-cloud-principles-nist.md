---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [nist, principles, self-service, multi-tenancy, elasticity, virtualisation]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Fundamental principles of the Cloud (per NIST)

The fundamental Cloud principles (which overlap strongly with the 'promises' of Chapter 1) aim to give users maximum flexibility and control without needing to engage with the technical complexity of the underlying infrastructure. The core principles:

- On-demand selfservice: direct access to compute, storage and networking without provider interaction - as simple as entering a credit card number and selecting the service. Example: auto-creating and scaling VMs (IaaS) on Azure or creating storage via Amazon S3.
- Plaats- en tijdonafhankelijk (location and time independent): access resources anywhere, anytime, with an internet connection. Example: Microsoft Azure Virtual Desktop.
- Resource pooling: providers divide resources like storage and compute across customers for efficient use of physical infrastructure. A VM's attached disk looks like a dedicated physical disk but is actually a small slice from an extremely large storage pool in a Cloud datacenter.
- Multi-tenancy: multiple organisations share the same infrastructure without access to each other's data (e.g. AWS EC2, Salesforce). In Azure a Tenant is 'your private piece of Cloud' - creating one makes you the 'tenant/renter' of a slice of Azure infrastructure.
- Virtualisatie: the backbone of Cloud computing - multiple VMs on one physical server. Hyper-V is a known example Microsoft itself uses; the concept also applies to storage, networking and more.
- Automatisering: eliminates manual processes for creating and partly managing resources via clear portals.
- Elasticiteit en schaalbaarheid: environments dynamically scale up for demand peaks and down again. Example: Netflix uses AWS to support millions of concurrent users during peaks like a popular new series launch.
- Gemeten diensten en pay-per-use: pay for the resources you use. You can also reserve capacity for one or three years for a discount on the normal per-minute price - a commercial twist that slightly contradicts the pure pay-per-use idea.

## Verwante notities

- [Bas deconstructs the cloud promises](bas-deconstructs-the-cloud-promises.md)
- [Bas's war story: SAN/NAS data migrations were weeks of nightmares](bas-san-nas-nightmares.md)
- [Cloud service models: SaaS, PaaS, IaaS, DaaS](cloud-service-models-saas-paas-iaas-daas.md)
- [Core cloud building blocks: datacenter, virtualization, APIs, storage, databases, elasticity](core-cloud-components-and-concepts.md)
- [How Bas teaches the five essential cloud characteristics](five-essential-cloud-characteristics-teaching.md)
- [The five NIST cloud characteristics](nist-cloud-characteristics.md)
- [NIST and its definition of Cloud computing](nist-cloud-definition.md)
- [The promises of the Cloud (and Bas's invitation to challenge them)](the-promises-of-the-cloud.md)
