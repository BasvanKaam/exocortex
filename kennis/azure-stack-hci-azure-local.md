---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [azure-stack-hci, azure-local, hybrid-cloud, edge-computing, azure-arc]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Azure Stack HCI (renamed Azure Local): cloud in your own datacenter

Azure Stack HCI (renamed Azure Local; Bas keeps the old name in the text) lets organisations use cloud benefits from their own datacenter, bridging local IT infrastructure and the Azure cloud. It runs modern cloud functionality 'locally' without moving data or applications to the public cloud.

It runs on Microsoft-certified HCI clusters (Hyper-Converged Infrastructure) from vendors like Dell, Lenovo and HP, placed in your datacenter and integrated by a Microsoft partner. Many of the most-used Azure services are supported and the UI looks virtually identical. AWS and GCP offer comparable solutions (Outposts and Local Zones from AWS; Distributed Cloud Edge from GCP).

As part of a hybrid strategy it lets companies run certain workloads on-prem while using public-cloud data/apps, gives a consistent experience (integrated with the Azure Portal, managed from one place), and enables edge computing. Benefits Bas lists include: native integration with Azure Backup/Monitor/Site Recovery/Security Center; unified management via Azure Arc and Windows Admin Center; optimisation for virtualization (clustered VMs, GPU integration, SDN); strong security (Secure VMs, encrypted storage); flexibility for VDI, SQL, AI/ML and Kubernetes containerisation; disaster recovery and high availability; modernising legacy apps; region/data compliance (keep data on-prem to meet local regulation and GDPR/AVG); and local hosting of Azure Virtual Desktop (AVD) for low-latency, data-sovereignty or compliance scenarios. Caveat: not all Azure AVD features are available via Azure Stack HCI / Azure Local.

## Bron-citaten (NL, verbatim)

> Met Azure Local haal je de kracht van de Azure Cloud in je datacenter.

## Verwante notities

- [Microsoft Azure Profile and Strengths](azure-profile-strengths.md)
- [Paper conclusion: Cloud only? Maybe never](bas-paper-conclusion-cloud-only-never.md)
- [Bas on the future limits of self-hosting your own data growth](bas-self-hosting-data-growth-limit.md)
- [Cloud deployment models (public, private, hybrid, community)](cloud-deployment-models.md)
- [Edge computing and Edge-nodes](edge-computing.md)
- [No universal Cloud standard, and the vendor lock-in problem](no-universal-cloud-standard-vendor-lock-in.md)
