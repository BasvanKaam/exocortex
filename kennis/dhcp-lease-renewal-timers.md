---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dhcp, lease-renewal, timers]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DHCP lease renewal timers

A client tries to renew when the lease is half over (50%, T1), asking the original server to keep the same address; the server resets the lease period and passes any changed configuration options. If that server does not respond, the client keeps using the address and sends another renewal request at 87.5% of the lease (T2), at which point any DHCP server may respond.

Durable concept.

*Bron: Core Knowledge doc 'DHCP Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DHCP 80/20 redundancy rule](dhcp-80-20-rule.md)
- [DHCP DORA lease process](dhcp-dora-lease-process.md)
- [DHCP relay agent across subnets](dhcp-relay-agent.md)
- [DHCP security threats](dhcp-security-threats.md)
- [DNS and DHCP Command-Line Tools](dns-dhcp-cli-tools.md)
