---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, tricerat, screwdrivers, wvd, print-server-proxy, cloud, azure]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Tricerat Print Server Proxy for Cloud/WVD printing

How it worked (2019). Tricerat's Simplify Print Suite plus ScrewDrivers technology lets WVD use advanced printing features without installing print drivers on WVD hosts (single or multi-user, Desktop or Server OS), for both client and network printers, managed from a single console covering WVD, on-prem, and other Cloud locations. The Print Server Proxy (introduced January 2018) is the key component for printing from WVD and remote Cloud locations: it's made of multiple sub-components and services, some living on-premises, with a constant Cloud-to-on-prem connection. It's designed to slot into existing infrastructure without opening many ports or rewriting firewall rules, and all traffic between proxy endpoints is encrypted and compressed.

## Architecture

The Print Server Proxy bridges on-prem print infrastructure to a WVD Azure tenant. Two services run on the on-prem print server: the Print Server Proxy Service and the normal Print Server Service. An Azure IaaS machine hosts the proxy service, a SQL database (for ScrewDriver) and licenses (~15-20 min to set up). The on-prem server polls the Azure server, maintaining a continuous connection; no vNet extension or VPN needed, only firewall ports 3550 and 3551.

## Print flow

User clicks print -> local ScrewDriver builds a virtual printer on the WVD machine -> job is converted to Tricerat's proprietary TriMeta Format (TMF), which adds compression and encryption -> forwarded to the Azure Print Server (proxy) -> sent to the on-prem print server/proxy where it is rendered to the printer's language (compression/encryption applied across the wire) -> delivered to the print device, where on the local network compression/encryption matter less. How it worked then: cross-cloud printing relied on a proxy plus proprietary format to compress and encrypt jobs over the WAN.

*Bron: blogpost 'A big step forward for Windows Virtual Desktop printing. Part one' (2019-06-26), basvankaam.com.*

*Bron: blogpost 'A big step forward for Windows Virtual Desktop printing. Part two' (2019-11-28), basvankaam.com.*

## Verwante notities

- [Why RDS Easy Print falls short for cloud/remote printing](easy-print-limitations-cloud.md)
- [RDS Easy Print and its limitations](rds-easy-print-limitations.md)
