---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [azure, rdp, endpoint, dns, networking]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Immutable names and per-VM RDP endpoints in classic Azure

How it worked then (2015): several Azure objects could not be renamed/relocated after creation - VM names, virtual network names, Cloud Service datacenter location, and a registered DNS server's name (Bas found he could not change a registered DNS server's IP in the virtual network). Management was via auto-created Endpoints: each VM got a different external port for RDP and PowerShell, so the right firewall ports had to be open or you could not reach the machine. From a restrictive customer site, RDP into an Azure VM often failed; changing a VM's RDP endpoint to port 443 (commonly allowed) could work, but only for one machine at a time since each needs its own endpoint. Static IPs had to be set via the preview portal or PowerShell, never manually inside the guest, or you would lose connectivity. NetScaler VPX was supported but only findable in the preview portal.

*Bron: blogpost 'How to: Get up to speed with Windows Azure. Deploying your personal test lab, fast!' (2015-06-22), basvankaam.com.*

## Verwante notities

- [Azure cost-control habits for a test lab](azure-classic-cost-control-takeaways.md)
- [Correct build order for an early Azure test lab](azure-classic-test-lab-build-order.md)
- [The Azure cloud hierarchy: tenant down to resources](azure-cloud-hierarchy.md)
- [Azure forced Microsoft's OS and application templates (2013)](azure-os-application-templates-2013.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
