---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dhcp, dora, lease, discover-offer-request-ack]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DHCP DORA lease process

The four-step DHCP lease handshake (DORA):

1. **DHCPDISCOVER**: the client broadcasts a request for an IP lease when it boots, asking any DHCP server to respond.
2. **DHCPOFFER**: one or more DHCP servers respond with an address offer.
3. **DHCPREQUEST**: the client tells the first server that responded that it wants that address; the other servers withdraw their offers.
4. **DHCPACK**: the chosen server acknowledges and assigns the IP address lease to the client.

Durable DHCP fundamental.

*Bron: Core Knowledge doc 'DHCP Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Classful IP addressing (historical reference)](classful-ip-addressing.md)
- [DHCP 80/20 redundancy rule](dhcp-80-20-rule.md)
- [DHCP lease renewal timers](dhcp-lease-renewal-timers.md)
- [DHCP relay agent across subnets](dhcp-relay-agent.md)
- [DHCP security threats](dhcp-security-threats.md)
- [DNS and DHCP Command-Line Tools](dns-dhcp-cli-tools.md)
- [RFC 1918 private IP address ranges](rfc1918-private-ip-ranges.md)
