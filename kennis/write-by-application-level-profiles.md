---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [profileunity, liquidware, registry-injection, user-profile]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Granular profile handling: write-by-application-level and registry injection

How it worked then (ProfileUnity, 2017): instead of treating NTUSER.DAT as one monolithic file, the tool scans the profile file by file and breaks registry data down to the tree, key, sub-key, value or data level for both HKCU and HKLM. At logoff it reviews the profile and only writes back changes for applications that were actually altered ('write by application level'), which reduces logoff times and avoids last-write-wins conflicts.

Loading works via 'registry injection': the NTUSER.DAT is not altered directly; registry information is injected through it (merge, replace, exclude) during or post login. Pre- and post-login trigger points let settings be saved or loaded on demand, e.g. when an application starts or closes. Simultaneous-login handling dated back to ProfileUnity 4.8 (~2011).

*Bron: blogpost 'The last write wins - NO, it does not, we do!' (2017-12-04), basvankaam.com.*

## Verwante notities

- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [Last write wins: why roaming profiles collide across sessions](last-write-wins-ntuser-dat.md)
- [Liquidware suite: ProfileUnity, FlexApp, Stratusphere UX (2018)](liquidware-profileunity-flexapp-stratusphere.md)
- [The non-persistent Office 365 / Outlook OST and search-index problem](non-persistent-outlook-search-ost-problem.md)
- [Profile Portability: an abstraction layer over the user profile](profile-portability-abstraction-engine.md)
- [ProfileUnity feature set and all-in-one model (2017)](profileunity-feature-overview-2017.md)
- [UEM should be simple, single-console, and not sold in tiers](uem-should-be-simple-no-modules.md)
- [Microsoft's 'one Windows 10 to rule them all' promise was false](windows-10-not-one-os-to-rule-them-all-2.md)
- [Windows user profile versions are not cross-compatible](windows-user-profile-version-incompatibility-2.md)
