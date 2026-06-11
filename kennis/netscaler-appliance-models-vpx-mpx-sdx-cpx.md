---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, vpx, mpx, sdx, cpx]
layer: reference
bron: inside-citrix-fma
---

# NetScaler appliance models: VPX, MPX, SDX, CPX

A NetScaler (ADC or Gateway) can be physical or virtual. Models:

- **VPX**: a virtual appliance running on your hypervisor of choice. Supported by Citrix for up to **1,500 concurrent ICA connections** (theoretically more).
- **MPX**: a physical appliance. Depending on the model it handles roughly **10,000 to 35,000 concurrent ICA connections**.
- **SDX**: a physical appliance running a customised/branded XenServer, capable of running multiple VPX appliances (up to **80**, depending on physical resources).
- **CPX**: Citrix's **containerized** NetScaler, mainly for testing and development; in tech preview at the time of writing.

There is also a free **VPX Express** edition, good for small deployments, PoCs and test environments — same features as VPX Standard but with limitations: no SSL offload, max 5 Mbps throughput, licensed per year. The main differences between physical models are compute resources and the **Cavium SSL accelerator card** used to encrypt/decrypt SSL traffic — a more powerful card handles more SSL transactions.

## Verwante notities

- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler ADC vs NetScaler Gateway editions](netscaler-adc-vs-gateway-2.md)
- [NetScaler ADC vs Gateway: same box, different license](netscaler-adc-vs-gateway-licensing.md)
- [NetScaler high availability and clustering](netscaler-high-availability-clustering.md)
- [NetScaler platforms, editions and HA](netscaler-platforms-and-licensing.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [NetScaler vServers, service objects and server objects](netscaler-virtual-server-service-server-objects.md)
