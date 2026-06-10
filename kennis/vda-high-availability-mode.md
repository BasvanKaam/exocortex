---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, high-availability, ica, registry, limitations]
layer: reference
bron: inside-citrix-fma
---

# VDA high-availability mode (direct ICA, last resort)

If the Central Site database is fine but the Delivery Controllers are unreachable, a VDA can be put into high-availability (HA) mode, accepting direct ICA connections from users instead of brokered connections, so users keep using their desktops/apps. Bas frames this as a last resort: 'Use the VDA in HA mode as a last resort. Hopefully it will never come to this.'

Behaviour: when communication with all Controllers fails, HA mode starts after a configurable period (default 300 seconds) and lasts a maximum of 30 days. During that time the VDA keeps trying to register; as soon as a Controller is available it re-registers without interrupting the user, and connections are brokered again. If it cannot register within 30 days, the desktop stops listening and becomes unavailable.

Per Citrix, HA mode suits only dedicated desktops with a known user-to-VDA mapping; it cannot be used for pooled desktops. Configure via two manually created registry keys: 'High Availability' (1 = enable, 0 = disable) and 'HaRegistrarTimeout' (time before HA kicks in). You must also supply each user with an ICA launch file (one per user); Citrix does not create or distribute these.

Limitations: user roaming (an already-connected device blocks connecting from another); Controller-originated policies (e.g. client drive mapping, clipboard) do not work, though Domain Controller and Local Group Policy still apply (outdated policies from a previous registration may persist); power management; and NetScaler Gateway / Remote Access cannot be used.

## Bron-citaten (NL, verbatim)

> Use the VDA in HA mode as a last resort. Hopefully it will never come to this.

## Verwante notities

- [The Central Site database in the FMA](central-site-database-fma.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [FMA Local Host Cache: Principal Broker, Secondary Broker (HA) and CSS](fma-local-host-cache-services.md)
- [FMA Zones VDA registration and Controller failover](fma-zones-vda-registration-and-failover.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [VDA registration: auto-update, fallback locations and the CBP](vda-registration-process.md)
