---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [hcl, abstraction-layer, api, hypervisor, host-connection]
layer: reference
bron: inside-citrix-fma
---

# FMA Hypervisor Communications Library (HCL) abstraction layer

The HCL is used by several FMA services (the Broker, Host and MCS services) to provide an abstract API for interacting with the underlying Host Connection(s). It ensures a consistent representation of the configured Host Connection including its network and storage resources.

Multiple supported hypervisors add code complexity; the HCL functions as an abstraction layer so that when a new hypervisor version is released or an existing one is altered, Citrix can quickly add support without replacing code in multiple places. The same applies to cloud platforms.

## Verwante notities

- [Host Connection key takeaways: MCS/PVS and cloud support](host-connection-mcs-pvs-cloud-support-key-takeaways.md)
- [Host Connections now support cloud, not just hypervisors](host-connections-cloud-support.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
