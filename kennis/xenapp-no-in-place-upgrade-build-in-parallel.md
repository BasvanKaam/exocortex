---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenapp, migration, farm, ima]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenApp Farms must be migrated in parallel, not upgraded in place (2013)

Citrix did not support an in-place upgrade to XenApp 6.5 from older versions because of fundamental product differences; you also cannot run a mixed Farm across 4.5/5.0, 6.0 and 6.5. The supported approach is to build a new 6.5 Farm alongside the old one and migrate resources across. Vocabulary Bas pins down: server upgrade (newer XenApp over existing), server migration (clean OS), Farm upgrade (existing Farm/Data Store kept), Farm migration (new Farm/Data Store).

Advantage of building in parallel: you get to redesign, e.g. move policies from IMA into Active Directory and start from scratch. Note also the quirk he calls out: 'XenApp 5.0' is effectively XenApp 4.5 with HRP5 installed.

*Bron: blogpost 'End of Life... to Migrate or not to Migrate?' (2013-04-28), basvankaam.com.*

## Verwante notities

- [Moving 32-bit to 64-bit (and 2003 to 2008) means app-compat work (durable lesson)](32bit-to-64bit-app-compat-is-a-fact-of-life.md)
- [XenApp migration tooling: Migration Center and 6.0-to-6.5 Upgrade Utility (2013)](xenapp-migration-tooling-2013.md)
