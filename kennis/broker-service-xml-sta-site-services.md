---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [broker, xml, sta, site-services, vda]
layer: reference
bron: inside-citrix-fma
---

# Broker service, XML/STA and the 18 site services

The Broker service includes both the XML and the STA services. There are 18 active (sub) site services in total, all running within the Broker service and handling various Site housekeeping tasks.

In the Desktop VDA the two main FMA services are PortICA (picaSvc2.exe / PicaSvc2.exe) and the Citrix Desktop Service (BrokerAgent.exe). The Connection Brokering Protocol (CBP) — a collection of WCF endpoints — plays an important role in VDA registration.

The Server VDA has no PortICA service but does have a Broker service. It reuses essentially the same ICA stack as XenApp 6.5 with a different management interface for compatibility with 7.x Delivery Controllers; installing it extends Microsoft's RDS protocol with the ICA/HDX feature set. Service groups make FMA services highly available.

## Verwante notities

- [The eighteen Broker Service Site services (distributed housekeeping)](fma-broker-eighteen-site-services.md)
- [Internal launch process: pooled VDI VM via StoreFront](internal-launch-process-pooled-vdi.md)
