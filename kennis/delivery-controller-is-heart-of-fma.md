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
