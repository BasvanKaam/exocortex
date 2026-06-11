---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [networking, subnetting, vlan, tcp-ip]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Subnetting and VLANs

**Subnetting**: an IP address splits into a network portion and a host portion. You design a subnet scheme by deciding how many networks you need and how many hosts per network, then borrowing bits accordingly (and noting whether the address is class A, B, or C). Each subnet is a separate network, logically isolated like a physical one; traffic between subnets passes through a default gateway, usually a router.

**VLAN**: a switch port is assigned to a VLAN, letting a logical LAN span geographically separated locations, floors, or buildings over the same physical switching. Each VLAN has its own subnet, mapping the layer-2 segmentation onto the layer-3 addressing.

*Bron: Core Knowledge doc 'Subnets and VLAN's Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Classful IP addressing (historical reference)](classful-ip-addressing.md)
- [DHCP relay agent across subnets](dhcp-relay-agent.md)
- [Host Name Resolution and Routing Process](host-routing-and-arp-process.md)
- [ISA Server 2004/2006 Configuration Concepts](isa-server-configuration-concepts.md)
- [Intranet Applications: the subnet objects that define split tunneling](netscaler-intranet-applications-object.md)
- [RFC 1918 private IP address ranges](rfc1918-private-ip-ranges.md)
