---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [kerberos, authentication, active-directory, reference]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Kerberos V5 Authentication

Kerberos (developed at MIT, named after the three-headed dog) is a three-party authentication scheme:

1. **Client**: the system/user making the request.
2. **Server**: the system offering a service to identity-confirmed systems.
3. **Key Distribution Center (KDC)**: the trusted intermediary that vouches for a client's identity. In a Windows domain the KDC runs on a DC.

Flow: the user supplies username, password, and domain (realm). The KDC authenticates and issues a **Ticket Granting Ticket (TGT)** — like a hand-stamp proving paid admission, so the user does not re-authenticate for every server. To reach a specific server the client presents its TGT to the KDC and requests a **session (service) ticket** for that server. Whether the client can actually access anything then depends on permissions.

Tickets expire on a group-policy-configurable schedule: default TGT (user ticket) lifetime 7 days, default session (service) ticket lifetime 10 hours.

In a multi-domain environment the client must obtain session tickets to traverse the trust path, requesting a ticket from a KDC in each domain along the path until it can request the final server's session ticket from a KDC in the server's domain. A session ticket for a server must be obtained from a KDC in the domain where that server lives.

*Bron: Core Knowledge doc 'AD Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Access Control: Security Descriptors, DACL, SACL](ad-access-control-descriptors.md)
- [AD Naming: UPN, SAM and SPN](ad-naming-upn-spn.md)
- [Active Directory Trust Types](ad-trust-types.md)
- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [SSL handshake: asymmetric to exchange, symmetric to transfer](ssl-handshake-symmetric-asymmetric.md)
- [Wireless Encryption: WEP, WPA and WPA2](wireless-encryption-wep-wpa-wpa2.md)
