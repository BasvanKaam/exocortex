---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, host-connection, mcs, pvs, zones]
layer: reference
bron: inside-citrix-fma
---

# Host Connection key takeaways: MCS/PVS and cloud support

Key points about Host Connections in XenDesktop/XenApp 7.x:

- Earlier 7.x releases limited Host Connections to hypervisors; cloud environments are now supported too.
- **MCS** works with Azure, AWS and the Citrix CloudPlatform, and with all the listed hypervisors. **PVS is not supported** in those clouds — it simply does not work.
- MCS only works with virtual machines.
- You can add multiple Host Connections, combining cloud and on-premises hypervisors.
- Hypervisor Host Connections use the addresses of your SCVMM, Virtual Center or XenCenter.
- When using **Zones**, make sure a Zone's Host Connection is close to, or physically located within, that Zone.

## Verwante notities

- [Citrix Host Connection](citrix-host-connection.md)
- [FMA Hypervisor Communications Library (HCL) abstraction layer](fma-hypervisor-communications-library.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [FMA Zones VDA registration and Controller failover](fma-zones-vda-registration-and-failover.md)
- [Host Connections now support cloud, not just hypervisors](host-connections-cloud-support.md)
- [Delivering Linux shared hosted desktops: controller, catalog and delivery group setup](linux-vda-controller-and-catalog-config.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
