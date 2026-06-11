---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [xenapp, session-sharing, registry, cdf, troubleshooting]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Detecting XenApp session sharing via the ICA Session registry key

How it worked then. Each XenApp session creates a unique key under `HKLM\Software\Citrix\Ica\Session\<session ID>\Connection`. When multiple application parameters appear there, session sharing succeeded. Each app carries an application state number:

- 0 = Published desktop or ICA listener (neither can be shared)
- 1 = Session is active
- 2 = Pre-launch session
- 3 = Lingering session
- 4 = Application not running

CDF (Citrix Diagnostic Facility) can trace XenApp components such as the Citrix Print Manager Service, smart cards and client drive mapping; have the user name, client name, server, session ID at hand to make the logs browsable.

*Bron: blogpost 'Troubleshooting one on one' (2013-01-17), basvankaam.com.*

## Verwante notities

- [Citrix policy precedence: IMA vs Citrix AD vs normal AD policies](citrix-policy-precedence-ima-ad.md)
