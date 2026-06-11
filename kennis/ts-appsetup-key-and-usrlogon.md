---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [terminal-server, citrix, registry, appsetup, userinit, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Terminal Server AppSetup key and UsrLogon.cmd (reference)

When Terminal Server is installed, UserInit.exe queries the registry key **AppSetup** at `HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon` and runs every program listed there.

By default this is just UsrLogon.cmd. MetaFrame XP adds cmstart.exe; MetaFrame version 3 adds CtxHide. UserInit then launches the user's shell from the registry (explorer.exe by default, changeable).

The AppSetup chain is where the Citrix seamless engine gets started, so a missing cmstart.exe entry means no seamless windows (though desktop sessions still work).

Dated reference for where the TS/Citrix logon hooks live in the registry.

*Bron: Core Knowledge doc 'Citrix TS Logon Proces Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix / Terminal Services logon sequence (reference)](citrix-ts-logon-sequence.md)
- [Citrix wfshell.exe, cltmgr.exe, and printer drivers (reference)](citrix-wfshell-cltmgr-printer-drivers.md)
- [Terminal Server install vs execute mode and the shadow key (reference)](terminal-server-install-vs-execute-mode-shadow-key.md)
- [The Terminal Server shadow key and registry sync at logon](terminal-server-shadow-key.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
