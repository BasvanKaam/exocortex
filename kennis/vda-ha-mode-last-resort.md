---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-16
tags: [citrix, vda, high-availability, opinion, inside-citrix]
bron: inside-citrix-book
---

# VDA HA mode is a last resort, not a design choice

Bas's stance: VDA high-availability mode (direct ICA when all Delivery Controllers are down) is purely an emergency option, not something you architect around. He frames it as "hard to imagine this ever happening" and a feature you use "as a last resort, hopefully it will never come to this." The real answer is the "one is none" rule: deploy redundant Delivery Controllers so you never reach the point where HA mode matters. Worth knowing the option exists; not worth depending on.

*Bron: Inside Citrix (2016), 'Inside Citrix ch7 - The Virtual Delivery Agent'.*

## Verwante notities

- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
- [One is none: always deploy two StoreFronts and two Delivery Controllers](one-is-none-storefront-dc-redundancy.md)
- [VDA high-availability mode (direct ICA fallback)](vda-high-availability-mode-2.md)
- [VDA high-availability mode for Controller outages](xd7-vda-high-availability-mode.md)
