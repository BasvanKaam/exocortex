---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [raid, storage, write-penalty, performance]
layer: reference
bron: inside-citrix-fma
---

# The RAID write penalty

RAID configurations bring a write penalty because a parity bit must also be written. A write can't be fully completed until both the data and the parity information are written to disk; the time taken to write the parity bit is the write penalty. This applies only to writes, not reads.
