---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dhcp, redundancy, 80-20, high-availability]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DHCP 80/20 redundancy rule

For redundancy across two DHCP servers on different subnets, split a scope so the local server holds ~80% of the addresses and a remote server holds ~20%. If the server holding 80% fails or is attacked, the other can still hand out addresses. This is a durable design pattern (the modern equivalent being DHCP failover, but the split-scope idea remains the reference).

*Bron: Core Knowledge doc 'DHCP Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DHCP DORA lease process](dhcp-dora-lease-process.md)
- [DHCP lease renewal timers](dhcp-lease-renewal-timers.md)
- [DHCP relay agent across subnets](dhcp-relay-agent.md)
- [DHCP security threats](dhcp-security-threats.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
