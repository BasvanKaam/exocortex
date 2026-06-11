---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [terminal-server, registry, shadow-key, install-mode, hkcu, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Terminal Server install vs execute mode and the shadow key (reference)

Applications write system-wide settings to HKLM and user-specific settings to HKCU. On a multi-user Terminal Server this is a problem: settings an installer writes to the installing user's HKCU would be missing for everyone else.

Every TS session runs in **execute mode** (normal) or **install mode**. Installing an app switches the session to install mode (historically via `change user /install`; Windows 2003 detects installs automatically). In install mode the server monitors the user's HKCU and mirrors any changes under HKCU\Software into a special HKLM key, `HKLM\Software\Microsoft\Windows NT\CurrentVersion\Terminal Server\Install\Software`, informally the **shadow key**. It holds the latest install-time settings that each user's HKCU\Software needs.

Dated, version-specific Terminal Server internals, captured as reference for how the shadow mechanism worked.

*Bron: Core Knowledge doc 'TS, Mem Usage, Shadow Key and (Flex) Profile Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Why adding new farm servers can wipe user app settings (shadow key timestamps)](shadow-key-new-farm-server-timestamp-trap.md)
- [Shadow key behavior on 64-bit and TSAWARE apps](shadow-key-wow64-and-tsaware.md)
- [Terminal Server registry mapping and the load-balancing timestamp trap](terminal-server-registry-mapping-timestamp-trap.md)
- [The Terminal Server shadow key and registry sync at logon](terminal-server-shadow-key.md)
- [Terminal Server AppSetup key and UsrLogon.cmd (reference)](ts-appsetup-key-and-usrlogon.md)
