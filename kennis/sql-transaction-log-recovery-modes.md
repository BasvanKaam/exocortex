---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [sql, transaction-log, recovery-mode, backup, central-site-database]
layer: reference
bron: inside-citrix-fma
---

# SQL Transaction-Log recovery modes for Citrix databases

The Transaction-Log records all transactions and modifications. If the live Site database becomes corrupt, the Transaction Log can be replayed to recreate it in a consistent state. This depends on the configured recovery mode:

- Simple Recovery mode: no log backups; no transaction log data saved. If the database fails, all changes since the last full backup must be redone.
- Full Recovery mode: requires backup logs; no work is lost and any point in time can be recovered. Needed for database mirroring.
- Bulk-Logged Recovery mode: an adjunct of full recovery permitting high-performance bulk copy operations; typically not used for Citrix databases.

With daily (or multiple-weekly) backups, Simple Recovery mode is usually sufficient. If Site configuration changes are constant, Full Recovery may be desirable. Always use high-performance storage (preferably SSDs) for SQL.
