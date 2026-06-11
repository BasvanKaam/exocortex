---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dhcp, security, rogue-dhcp, dos]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DHCP security threats

Common DHCP threats:

- Address-exhaustion denial-of-service: an attacker requests and obtains a large number of leases.
- DoS via a flood of DNS dynamic updates through the DHCP server.
- A rogue DHCP server handing clients incorrect configuration.
- Leaking DNS/WINS server addresses via DHCP options, which an attacker can use to target those servers.

Mitigations noted: authorize DHCP servers in Active Directory and back up the DHCP database. Durable concerns, though AD authorization is a Windows-specific control.

*Bron: Core Knowledge doc 'DHCP Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Current cyber threats and 2025+ trends](current-cyber-threats-and-2025-trends.md)
- [DHCP 80/20 redundancy rule](dhcp-80-20-rule.md)
- [DHCP DORA lease process](dhcp-dora-lease-process.md)
- [DHCP lease renewal timers](dhcp-lease-renewal-timers.md)
- [DHCP relay agent across subnets](dhcp-relay-agent.md)
- [DNS and DHCP Command-Line Tools](dns-dhcp-cli-tools.md)
- [Wireless Encryption: WEP, WPA and WPA2](wireless-encryption-wep-wpa-wpa2.md)
