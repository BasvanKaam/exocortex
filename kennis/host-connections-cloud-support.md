---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [host-connection, cloud, azure, aws, nutanix]
layer: reference
bron: inside-citrix-fma
---

# Host Connections now support cloud, not just hypervisors

Earlier 7.x releases limited Host Connections to hypervisor platforms; cloud environments are now supported too. MCS works with Azure, AWS and the Citrix CloudPlatform (PVS does not work there), and with all supported hypervisors; the Nutanix Acropolis Hypervisor will be added shortly as a Host Connection option. You can add multiple Host Connections, mixing cloud and on-premises. When adding hypervisor connections you use the address of your System Center Virtual Machine Manager, vCenter or XenCenter. With Zones, keep a Zone's Host Connection physically close to or within that Zone.
