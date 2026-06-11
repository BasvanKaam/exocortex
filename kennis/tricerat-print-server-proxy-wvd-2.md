---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, tricerat, wvd, azure, screwdrivers]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Tricerat Print Server Proxy architecture for WVD printing

Tricerat's Print Server Proxy (introduced Jan 2018), with the Simplify Printing Suite and ScrewDriver technology, bridges on-prem print infrastructure to a WVD Azure tenant. Two services run on the on-prem print server: the Print Server Proxy Service and the normal Print Server Service. An Azure IaaS machine hosts the proxy service, a SQL database (for ScrewDriver) and licenses (~15-20 min to set up). The on-prem server polls the Azure server, maintaining a continuous connection; no vNet extension or VPN needed, only firewall ports 3550 and 3551.

Print flow: user clicks print -> local ScrewDriver builds a virtual printer on the WVD machine -> job is converted to Tricerat's proprietary TriMeta Format (TMF), which adds compression and encryption -> forwarded to the Azure Print Server (proxy) -> sent to the on-prem print server/proxy where it is rendered to the printer's language (compression/encryption applied across the wire) -> delivered to the print device, where on the local network compression/encryption matter less. How it worked then: cross-cloud printing relied on a proxy+proprietary format to compress and encrypt jobs over the WAN.

*Bron: blogpost 'A big step forward for Windows Virtual Desktop printing. Part two' (2019-11-28), basvankaam.com.*
