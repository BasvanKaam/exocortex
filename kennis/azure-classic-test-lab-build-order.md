---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure, test-lab, virtual-network, storage-account, cloud-service, citrix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Correct build order for an early Azure test lab

How it worked then (2015, Azure Service Management / "classic" portal at manage.windowsazure.com): spinning up VMs first gets you nowhere. The correct order Bas documented was: (1) create an Azure Cloud Service, choosing the datacenter region carefully because it cannot be changed afterward (his was West Europe); (2) create a Virtual Network (your private, isolated network on Azure); (3) create a Storage Account where VM VHDs live; (4) create VMs via the "From Gallery" path so you can attach the existing Cloud Service, virtual network and storage account (Quick Create spawns separate ones automatically); (5) build the domain controller / DNS; (6) register the DNS server's name and IP back in the virtual network properties. A Cloud Service could hold up to 50 VMs. No DHCP is needed; the virtual network handles addressing. The classic vs preview portal split mattered: some features (static IP assignment, NetScaler VPX) only existed in the preview portal.

*Bron: blogpost 'How to: Get up to speed with Windows Azure. Deploying your personal test lab, fast!' (2015-06-22), basvankaam.com.*

## Verwante notities

- [Azure cost-control habits for a test lab](azure-classic-cost-control-takeaways.md)
- [Immutable names and per-VM RDP endpoints in classic Azure](azure-classic-immutable-names-and-rdp-endpoints.md)
- [The Azure cloud hierarchy: tenant down to resources](azure-cloud-hierarchy.md)
- [Azure forced Microsoft's OS and application templates (2013)](azure-os-application-templates-2013.md)
- [Forcing Microsoft Security Essentials onto Server 2012 (home lab)](mse-on-server-2012-workaround.md)
- [Positie: the Citrix XD7-on-Azure design guide was misleading marketing](positie-citrix-azure-design-guide-confusing-2013.md)
