---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dns, resource-records, soa, mx, srv, ptr]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DNS resource record types

Common DNS resource records:

- **SOA (Start of Authority)**: first record in the zone; holds zone properties such as the primary DNS server and the database version (serial) number.
- **NS (Name Server)**: lists the authoritative DNS servers for a domain and for any delegated subdomains.
- **A (Host)**: maps an FQDN to a 32-bit IPv4 address.
- **CNAME (Alias)**: ties an alias to its canonical domain name; useful for hiding network detail from clients.
- **MX (Mail exchanger)**: identifies the mail servers handling email for a domain, with priority for backups.
- **PTR (Pointer)**: used in reverse lookups to map an IP back to a host name/FQDN.
- **SRV (Service location)**: used by Active Directory to locate domain controllers, LDAP servers, and global catalog servers.

The SOA fields: source host, contact email, serial number, refresh time, retry time, expiration time, and time-to-live (caching).

Durable DNS fundamentals.

*Bron: Core Knowledge doc 'DNS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Naming: UPN, SAM and SPN](ad-naming-upn-spn.md)
- [DNS caching: server and client](dns-caching-server-and-client.md)
- [DNS conditional forwarders](dns-conditional-forwarders.md)
- [DNS recursion vs iteration and root hints](dns-recursion-vs-iteration.md)
- [DNS reverse lookup and in-addr.arpa](dns-reverse-lookup-in-addr-arpa.md)
- [DNS zone transfer and Notify](dns-zone-transfer-and-notify.md)
- [DNS zone types](dns-zone-types.md)
- [Exchange Message Size Limit Precedence](exchange-message-size-limit-precedence.md)
- [NetScaler GSLB is DNS-based multi-site traffic management](netscaler-gslb-dns-foundation.md)
- [Windows name resolution order: DNS and NetBIOS/WINS (reference)](windows-name-resolution-order-dns-netbios.md)
