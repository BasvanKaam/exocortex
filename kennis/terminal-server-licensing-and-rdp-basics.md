---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [terminal-server, rdp, licensing, tscal, session-directory, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Terminal Server licensing and RDP basics (reference)

Key facts captured for classic Terminal Server:

- **RDP** uses 128-bit encryption and the TS component listens on TCP port **3389**.
- **Session Directory** stores remote session info and is used to reconnect interrupted/disconnected sessions.
- **Licensing**: per-device CALs; a device gets a temporary token the first time it connects to a license server, with a 120-day grace period. License server discovery uses a registry key and an LDAP query, then contacts the license server over RPC; on success the registry key is updated.
- **Session 0** was the console session.

The TS logon/session sequence: encryption level established, licensing negotiated, RDP stack mapped to an existing user session, logon screen presented, smss.exe creates a new session space, WinLogon authenticates the account, and the TS service maintains a domain\username-to-session-ID list so a returning user is remapped into their existing session.

Dated, version-specific reference (port 3389 and the RDP concept remain current).

*Bron: Core Knowledge doc 'TS, Mem Usage, Shadow Key and (Flex) Profile Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix / Terminal Services logon sequence (reference)](citrix-ts-logon-sequence.md)
- [From Terminal Services to AVD - The Multi-User History](history-terminal-services-to-avd.md)
- [ICA protocol origin and the birth of Microsoft RDP](ica-protocol-origin-and-rdp.md)
- [Microsoft RDS CALs and the XenApp vs XenDesktop split](microsoft-rds-cals-with-xenapp.md)
- [How Microsoft RDP descended from Citrix's ICA](rdp-descended-from-citrix-ica.md)
