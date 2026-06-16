---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [windows, user-profile, migration, windows-10, profile, profile-versions]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Windows user profile versions are incompatible across OS releases

How it worked then (2017). Windows XP / Server 2003 introduced the mechanism that loads and stores the user profile; that was profile version 1.0. Each major OS release bumped the version, reaching v6.0 with Windows 10 / Server 2016. The versions are not interchangeable: a profile created on Windows 7 / Server 2008 R2 (v2) cannot be used on Windows 8 / Server 2012, and a Windows 7 profile is incompatible with Windows 10 (v5/v6). Logging in with an older profile version on a newer OS triggers 'The user profile cannot be loaded' and a blank default profile loads instead, so the user loses their settings and data.

Critically, new Windows 10 feature updates can also introduce new profile versions, so even an in-place Windows 10 update can silently break profiles. Microsoft has in cases claimed no version difference between two Windows 10 builds (e.g. 1607 and 1703, both reported v6.0) while in practice users still lost all personal settings after the upgrade.

Lesson: do not trust the documented version number; test profile compatibility thoroughly before rolling out a Windows 10 update.

*Bron: blogpost 'Probleem - Windows 10 blijkt niet het beloofde 'One OS to rule them all'. Gebruikersprofiel versies blijven wijzigen' (2017-11-10), basvankaam.com.*

*Bron: blogpost 'In detail. Windows 10, the one OS to rule them all - Except it's NOT' (2017-12-20), basvankaam.com.*
