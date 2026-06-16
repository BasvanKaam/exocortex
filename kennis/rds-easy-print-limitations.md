---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, rds, easy-print, wvd, universal-print-driver]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# RDS Easy Print and its limitations

How it worked. Easy Print, Microsoft's RDS printing solution introduced with Windows Server 2008, maps client printers into an RDS session using the Easy Print universal print driver, so you don't need separate drivers per redirected printer. Limitations Bas highlights: it is specific to client printer redirection and does NOT work for network printers; it cannot be set as default (Microsoft-native drivers get auto-installed when the server detects a new device with no compatible driver on board); and being a universal solution, advanced/rich printing features aren't available. These gaps are where third-party suites like Tricerat position themselves.

*Bron: blogpost 'A big step forward for Windows Virtual Desktop printing. Part one' (2019-06-26), basvankaam.com.*

## Verwante notities

- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [Why RDS Easy Print falls short for cloud/remote printing](easy-print-limitations-cloud.md)
- [Printing is business critical, and underrated](printing-is-business-critical.md)
- [Tricerat Print Server Proxy for Cloud/WVD printing](tricerat-print-server-proxy-wvd.md)
- [Universal Print: moving print to the M365 cloud](universal-print-cloud-print-concept.md)
