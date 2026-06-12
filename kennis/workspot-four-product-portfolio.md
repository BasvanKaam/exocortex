---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [workspot, daas, vdi, azure, wvd, cloud-native, cgit, vendor-review]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# Workspot's cloud-born portfolio: Desktop/Workstation/App/DR Cloud

Part 3 of Bas's series on cloud-born alternatives for delivering apps and desktops reviews Workspot, a 'born-in-the-cloud' vendor focused on simplifying VDI. Key facts as of the post:

- **Management plane is Azure-only**, hosted by Workspot in Azure and not deployable on-premises (AWS was an option in some US regions). This mirrors CloudJumper from part 2.
- **Two flagship DaaS products, both Azure-only:** Desktop Cloud (everyday workloads) and Workstation Cloud (heavy, graphics-intensive workloads, using Azure GPU VMs driven by NVIDIA technology). 'Plain' VDI/RDSH environments can sit in the cloud or on-premises in your own datacenter.
- **WVD integration is partial:** Workspot is a Microsoft WVD partner; it can use, automatically deploy and maintain the Windows 10 Enterprise multi-session image, but integration stops there.
- **Strength is automated build/maintain of DaaS and VDI platforms.** On-prem they partner with 3-tier vendors (HP, Cisco, NetApp, Dell) and hyperconverged vendors (Nutanix, HP, Hypergrid, Scale). This combo is branded 'Workspot Hybride Cloud'. Workspot claims a fully operational VDI platform in days rather than weeks/months.
- **App Cloud** is published-applications-as-a-service (Bas's joke: 'PaaaS?'): deliver a set of apps without owning the RDS/VDI farm, architecture or images. Azure-only.
- **Disaster Recovery Cloud** keeps a configurable number of up-to-date Windows 10 VMs on stand-by for physical-PC DR, activatable with one click (you still need a separate physical device to work from).
- **Commercials:** named and concurrent licenses, no minimum quantity, from $20, via Azure Marketplace or partner channels. Other OS licenses (Windows 10, Server 2016/2019) are BYOL. Basic support included, premium available.

*Bron: CGIT-blog 'Workspot, Cloud native Apps, VDI en RDSH – deel 3' (CGIT).*

*Bron: Salomon-IT 'Workspot, Cloud native Apps, VDI en RDSH – deel 3' (CGIT Blogs).*

## Verwante notities

- [CloudJumper portfolio: CWMS, CW for Azure, and WVD integration](cloudjumper-portfolio-cwms-cw-for-azure-wvd.md)
- [DaaS vs VDI vs RDSH delivery models](daas-vdi-rdsh-delivery-models.md)
- [EUC alternatives feature comparison (CloudJumper, Workspot, Parallels)](euc-vendor-comparison-matrix-2019.md)
- [Session proposition: five (cloud) alternatives to Citrix and VMware](five-cloud-alternatives-to-citrix-vmware-session.md)
- [Position: Workspot's aggressive anti-Citrix positioning is a mistake](workspot-anti-citrix-marketing-is-a-mistake.md)
- [Workspot cloud DaaS](workspot-cloud-daas.md)
