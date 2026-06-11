---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [ip, classful, address-classes, subnetting, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Classful IP addressing (historical reference)

The historical classful network architecture, by first octet:

- **Class A**: first octet 0–127, binary 0xxxxxxx, network ID = a, host = b.c.d; 128 networks, 16,777,216 addresses each.
- **Class B**: first octet 128–191, binary 10xxxxxx, network ID = a.b, host = c.d; 16,384 networks, 65,536 addresses each.
- **Class C**: first octet 192–223, binary 110xxxxx, network ID = a.b.c, host = d; 2,097,152 networks, 256 addresses each.

Classful addressing was superseded by CIDR, so this is historical reference, but it remains the conceptual foundation for understanding address classes and subnetting.

*Bron: Core Knowledge doc 'DHCP Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DHCP DORA lease process](dhcp-dora-lease-process.md)
- [Host Name Resolution and Routing Process](host-routing-and-arp-process.md)
- [RFC 1918 private IP address ranges](rfc1918-private-ip-ranges.md)
- [Subnetting and VLANs](subnetting-and-vlans.md)
