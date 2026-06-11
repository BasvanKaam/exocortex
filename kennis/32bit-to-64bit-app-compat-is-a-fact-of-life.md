---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [migration, app-compatibility, windows-server, planning]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Moving 32-bit to 64-bit (and 2003 to 2008) means app-compat work (durable lesson)

Bas hammers a recurring migration truth: when you move from a 32-bit OS to a 64-bit OS "you will eventually run into application compatibility issues, it's a fact of life!" The same applies crossing from Server 2003 to Server 2008 regardless of bitness, because 2008 is fundamentally different (UAC, Windows Resource Protection, IE security restrictions). His practical advice: either migrate from an already-64-bit Server 2008 source so you avoid app-compat surprises, or do it all at once from the oldest platform and address everything in one go. Don't underestimate this work item - it's the time sink in any platform migration, a lesson that outlives the specific Windows versions.

*Bron: blogpost 'End of Life... to Migrate or not to Migrate?' (2013-04-28), basvankaam.com.*

## Verwante notities

- [Delivering five Windows generations from one infrastructure](five-generations-of-windows-one-infrastructure.md)
- [Greenfield onboarding is a utopia; plan for existing profiles and data](migration-greenfield-utopia-vs-brownfield.md)
- [OS Migration Is More Than Swapping the OS](os-migration-is-more-than-the-os.md)
- [Shadow key behavior on 64-bit and TSAWARE apps](shadow-key-wow64-and-tsaware.md)
- [Windows user profile versions are incompatible across OS releases](windows-user-profile-version-incompatibility.md)
- [XenApp Farms must be migrated in parallel, not upgraded in place (2013)](xenapp-no-in-place-upgrade-build-in-parallel.md)
- [XP end-of-life is the moment to innovate, not just migrate](xp-eol-act-now-position.md)
