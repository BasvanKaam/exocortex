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

## Verwante notities

- [Citrix Host Connection](citrix-host-connection.md)
- [Citrix Workspace Cloud as the hybrid bridge](citrix-workspace-cloud-hybrid-model.md)
- [Citrix Lifecycle Management Services and blueprints](cwc-lifecycle-management-services.md)
- [FMA Hypervisor Communications Library (HCL) abstraction layer](fma-hypervisor-communications-library.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [Host Connection key takeaways: MCS/PVS and cloud support](host-connection-mcs-pvs-cloud-support-key-takeaways.md)
- [Machine Creation Services essentials](machine-creation-services-essentials.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
