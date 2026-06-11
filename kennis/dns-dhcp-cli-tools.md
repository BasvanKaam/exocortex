---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, dhcp, cli, networking]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# DNS and DHCP Command-Line Tools

- **DNS**: `Dnscmd.exe` does most of what the DNS MMC snap-in does - create/delete/view zones and records, reload/refresh/pause/resume zones, clear the cache, manage root hints, and start/stop the service. `Nslookup` query-tests the namespace and shows config. `Ipconfig /registerdns | /flushdns | /displaydns` manage the client resolver cache.
- **DHCP**: `Ipconfig /all | /renew | /release` on the client; `Netsh dhcp server \\servername` for server-side administration.

*Bron: Core Knowledge doc 'Command - line Tooling Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Domain Controller Health-Check CLI Routine](dc-health-check-cli-routine.md)
- [DHCP DORA lease process](dhcp-dora-lease-process.md)
- [DHCP lease renewal timers](dhcp-lease-renewal-timers.md)
- [DHCP relay agent across subnets](dhcp-relay-agent.md)
- [DHCP security threats](dhcp-security-threats.md)
- [Windows name resolution order: DNS and NetBIOS/WINS (reference)](windows-name-resolution-order-dns-netbios.md)
