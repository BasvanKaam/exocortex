---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [microsoft, security-essentials, server-2012, antivirus, homelab]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Forcing Microsoft Security Essentials onto Server 2012 (home lab)

How it worked then (2015): Microsoft Security Essentials is neither supported nor installable on Server 2012 by default. The workaround Bas documents: right-click mseinstall.exe, set Compatibility mode to Windows 7, then run it from an elevated command prompt with the /disableoslimit parameter. Important caveat he adds after reader pushback: this does NOT give full protection on a server OS and must not be used in production, nor in a test environment that mirrors something heading to production, it was strictly for his single-server home lab. The 'proper' answer (per a commenter) is System Center Endpoint Protection. Free alternatives that DO support Server 2012: ClamWin, Immunet, Avira, and SCCM 2012 Endpoint Protection if you have an MSDN membership. Separate fix in the same post: a TP-LINK wireless adapter failing on Server 2012 was resolved by enabling the 'Wireless LAN Service' feature and reinstalling the drivers. Dated home-lab tinkering.

*Bron: blogpost 'Running Microsoft Security Essentials on Server 2012' (2015-01-20), basvankaam.com.*

## Verwante notities

- [Correct build order for an early Azure test lab](azure-classic-test-lab-build-order.md)
- [Using CentOS 6.6 to test the Citrix Linux VDA (unsupported but code-close to RHEL)](linux-vda-centos-unsupported-but-usable-for-testing.md)
- [The undocumented 'restart additional groups' staggers reboots](restart-additional-groups-undocumented.md)
- [Server 2012 .NET 3.5 Feature on Demand install gotcha (how it worked then)](server-2012-net35-feature-on-demand-gotcha.md)
- [Why adding new farm servers can wipe user app settings (shadow key timestamps)](shadow-key-new-farm-server-timestamp-trap.md)
