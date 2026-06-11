---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [active-directory, upn, spn, naming, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# AD Naming: UPN, SAM and SPN

Naming conventions in Windows Server 2003-era AD:

- Each user account has a logon name, a pre-Windows 2000 logon name (SAM account name, suggested from the first 20 bytes of the logon name), and a UPN suffix.
- The **UPN** follows IETF RFC 822: logon name + "@" + UPN suffix. AD adds the @ automatically; more than one @ is invalid. The default suffix is the DNS name of the domain where the account was created. An alternative UPN suffix can be created (need not be a valid DNS name) to shorten logon names in deeply nested domain trees and improve logon security.
- Each computer account has a relative DN, a pre-Windows 2000 computer name (first 15 bytes of the SAM name), a primary DNS suffix, a DNS host name (FQDN), and an SPN.
- The **SPN** (Service Principal Name) is a multi-valued attribute usually built from the host's DNS name, used during mutual client/server authentication; the client locates a computer account by the SPN of the service it wants to reach. The SPN can be changed only by Domain Admins.

Pre-Windows 2000 logon (DOMAIN\Username) remains usable for older clients.

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Access Control: Security Descriptors, DACL, SACL](ad-access-control-descriptors.md)
- [Active Directory Trust Types](ad-trust-types.md)
- [DNS resource record types](dns-resource-record-types.md)
- [Kerberos V5 Authentication](kerberos-v5-authentication.md)
