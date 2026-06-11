---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [igel, thin-client, udc3, ud-pocket, endpoint]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# IGEL UDC3 vs UD Pocket: permanent vs temporary thin-client conversion

How it worked in 2018. IGEL offered two software products to turn existing x86 hardware into managed thin clients running the IGEL Universal Desktop Linux OS (then in its 6th generation):

- UD Pocket: a small hardened dual-boot USB stick. Boot the machine from it and it becomes a thin client within ~15-20 seconds, without touching the installed OS or data on disk (the Pocket runs entirely from USB). Temporary and reversible. Ideal for remote/mobile workers and contractors needing on-demand VDI access.
- UDC3 (Universal Desktop Converter): firmware that permanently replaces the existing Windows or Linux OS, wiping it from disk and effectively hiding the physical HDD/SSD from the user (more secure, harder to tamper with). Permanent. Conversion takes roughly two to three minutes depending on CPU.

Minimum requirements for both: 64-bit x86 processor, 2 GB RAM, 2 GB flash/HDD, USB boot support. In practice any PC or laptop built within the previous ~6 years, plus Macs and even existing thin clients. UDC3 could also be installed onto a bootable USB stick when the target OS had to stay intact. Both ship with the IGEL Universal Management Suite (UMS) for central configuration and management.

*Bron: blogpost 'IGEL UDC3 converts machines into thin clients' (2018-08-16), basvankaam.com.*

## Verwante notities

- [IGEL Citrix Ready and HDX Ready certification (2018)](igel-citrix-ready-hdx-ready.md)
- [IGEL is a software company, not just a thin-client maker](igel-is-a-software-company-now.md)
- [IGEL UD Pocket: a USB stick that turns any PC into a thin client](igel-ud-pocket-usb-thin-client.md)
- [IGEL UMS can manage Windows endpoints, not just IGEL thin clients](igel-ums-manages-windows-endpoints.md)
- [IGEL UMS: central thin client management via profiles and directories](igel-ums-thin-client-management.md)
