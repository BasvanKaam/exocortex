---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-16
tags: [citrix, vda, registration, auto-update, fma, inside-citrix]
layer: reference
gedateerd: ja
bron: inside-citrix-book
---

# VDA registration and Controller discovery order

How it worked in the XenDesktop 7.x FMA era. On boot the VDA tries to register with one of the Site's Delivery Controllers (default port 80, changeable via the VDA's Control Panel settings). To know which Controllers exist, the default mechanism is the `auto-update` feature (enabled by default), which keeps every VDA's persisted Controller list current as Controllers are added or go offline.

When auto-update is disabled or returns bad data, the VDA falls back through these locations in order:
1. Configured policies
2. The `ListOfDDCs` registry key
3. OU-based discovery (legacy)
4. The `Personality.ini` file created by MCS

Verify a successful registration by restarting the Citrix Desktop Service on the VDA and looking for event 1012 ("successfully registered with a Delivery Controller"). A VDA that can't register stays in an unregistered state: not accessible or manageable through any Controller.

*Bron: Inside Citrix (2016), 'Inside Citrix ch7 - The Virtual Delivery Agent'.*

## Verwante notities

- [Citrix Cloud Connector replaces the on-prem Delivery Controller as broker](citrix-cloud-connector-as-broker.md)
- [Delivery Controller as the heart of the FMA](delivery-controller-is-heart-of-fma.md)
- [VDA high-availability mode (direct ICA fallback)](vda-high-availability-mode-2.md)
- [The VDA: client-side component, services and registration](vda-overview-services-and-registration.md)
- [VDA registration: auto-update, fallback locations and the CBP](vda-registration-process.md)
- [Troubleshooting the VDA registration process and Citrix Health Assistant](vda-registration-troubleshooting.md)
- [Zone VDA registration and failover behaviour (7.7)](zones-vda-registration-failover.md)
