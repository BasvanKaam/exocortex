---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, terminal-server, ica, logon, winlogon, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix / Terminal Services logon sequence (reference)

The ICA logon chain, however the session is invoked (Program Neighborhood, Web Interface, double-clicking an .ICA file):

1. **ICA client engine** (wfica32.exe on Win32) loads module.ini from the ICA client root, which defines the client's capabilities/virtual drivers.
2. **ICA handshake** over port 1494 (even with session reliability enabled); the server answers "7F7FICA" and the client sends its list of supported virtual channels.
3. **TSCAL license** verification. If the license cannot be verified the session simply ends, which is by design but confusing.
4. **WinLogon.exe** calls the GINA (plus linked GINAs such as ctxgina.dll when MetaFrame is installed); the user logs on and rights are checked via csrss.exe.
5. **UserInit.exe** sets up the environment and executes everything listed in the AppSetup registry key (see separate note), then launches the shell (explorer.exe by default).
6. Run-once keys, Startup folder, logon scripts, and Citrix license checks complete.
7. **WinLogon.exe** downloads the user profile: it asks the logon server (DC) whether a roaming profile is configured, checks for a local copy, compares timestamps, and copies the roaming profile down if the remote copy is newer.
8. **GPOs**: the server contacts the logon server for user GPOs, downloads and applies them, handles filtering/recursion, processes extensions (folder redirection, security policy, disk quota), and launches any apps specified in policy.

Dated reference for the classic XenApp/MetaFrame era logon flow.

*Bron: Core Knowledge doc 'Citrix TS Logon Proces Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix wfshell.exe, cltmgr.exe, and printer drivers (reference)](citrix-wfshell-cltmgr-printer-drivers.md)
- [The origin of Citrix and the ICA protocol](history-of-citrix-and-ica.md)
- [What the ICA protocol does and its default ports](ica-protocol-fundamentals.md)
- [Terminal Server licensing and RDP basics (reference)](terminal-server-licensing-and-rdp-basics.md)
- [Terminal Server / Citrix troubleshooting checklist (own notes)](terminal-server-troubleshooting-checklist.md)
- [Terminal Server AppSetup key and UsrLogon.cmd (reference)](ts-appsetup-key-and-usrlogon.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
