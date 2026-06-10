---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [delivery-controller, fma, architecture, design]
layer: rich
bron: inside-citrix-fma
---

# Delivery Controller as the heart of the FMA

Bas frames the Delivery Controller(s) as the heart of an FMA deployment because almost all Site traffic flows directly through them to the Central Site database and back. His practical guidance:

- Always deploy at least two Delivery Controllers per Site, and per Zone where possible (a minimum of one per Zone is needed in case of a WAN link failure).
- Virtualise them for flexibility, especially in bigger environments, so adding extra DCs or compute is a breeze.
- Keep them physically close to the database server and any Host Connections.
- Do not install SQL on the same machine as a Delivery Controller.

He stresses Delivery Controllers are fundamentally different from the old Data Collectors: no Local Host Cache, direct database communication, no communication between Delivery Controllers, and a service-/agent(VDA)-based model.

## Verwante notities

- [The XenDesktop Central Site database](central-site-database-role.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [Delivery Controller server sizing and supported OS](delivery-controller-sizing.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
