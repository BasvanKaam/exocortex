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
