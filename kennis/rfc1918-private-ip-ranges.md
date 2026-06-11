---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [ip, rfc1918, private-addresses, nat, iana]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# RFC 1918 private IP address ranges

Private IP addresses are used on internal networks and are not routable on the public Internet. IANA reserved three ranges in RFC 1918 for private use:

- 10.0.0.0 – 10.255.255.255
- 172.16.0.0 – 172.31.255.255
- 192.168.0.0 – 192.168.255.255

(The source note wrote the first range's upper bound as 10.25.255.255, a typo for 10.255.255.255.) Hosts reach the Internet from these addresses via NAT. Durable networking fundamental.

*Bron: Core Knowledge doc 'DHCP Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Classful IP addressing (historical reference)](classful-ip-addressing.md)
- [DHCP DORA lease process](dhcp-dora-lease-process.md)
- [Host Name Resolution and Routing Process](host-routing-and-arp-process.md)
- [NetScaler IP addresses: NSIP, SNIP and MIP](netscaler-ip-addresses-nsip-snip-mip.md)
- [Subnetting and VLANs](subnetting-and-vlans.md)
