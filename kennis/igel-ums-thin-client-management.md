---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [igel, ums, thin-client, management, profile]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# IGEL UMS: central thin client management via profiles and directories

How it worked then. IGEL Universal Management Suite (UMS) centrally configures, manages and partly monitors IGEL devices. Devices must first be 'known' to UMS via network scan, CSV import, manual or automatic registration; on registration a server certificate is stored on the device so only the holder of the private key can manage it. Devices are organised in a directory/structure tree (by location, profile or company structure), and Profiles (standard, template, master) apply predefined configurations at directory/group or individual level. Bas frames it by analogy to Active Directory: a profile is like a policy, directories are like organizational units, and AD can be linked to UMS to import users as administrator accounts. Firmware customizations sit between master and standard profiles in priority.

*Bron: blogpost 'The IGEL UD Pocket. At only 3.3 grams, the world's smallest and lightest thin client' (2017-09-12), basvankaam.com.*

## Verwante notities

- [Citrix policy precedence: IMA vs Citrix AD vs normal AD policies](citrix-policy-precedence-ima-ad.md)
- [Good, fast AND cheap is achievable, not an impossible triangle (with IGEL)](good-fast-cheap-is-achievable-igel.md)
- [IGEL Citrix Ready and HDX Ready certification (2018)](igel-citrix-ready-hdx-ready.md)
- [IGEL is a software company, not just a thin-client maker](igel-is-a-software-company-now.md)
- [IGEL UD Pocket: a USB stick that turns any PC into a thin client](igel-ud-pocket-usb-thin-client.md)
- [IGEL UDC3 vs UD Pocket: permanent vs temporary thin-client conversion](igel-udc3-vs-ud-pocket.md)
- [IGEL UMS can manage Windows endpoints, not just IGEL thin clients](igel-ums-manages-windows-endpoints.md)
