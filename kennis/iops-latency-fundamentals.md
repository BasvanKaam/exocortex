---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [storage, iops, latency, vdi, performance, hdd, ssd]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# IOPS fundamentals: latency is king

Durable storage concepts (written 2014 for VDI, still broadly valid):

- IOPS = input/output operations per second (read or write). Being able to *issue* 100 IOPS is not the same as *processing* them; processing takes time, and that time is latency. A disk that issues 100 IOPS but processes each at 20ms only truly handles ~50/sec.
- A raw IOPS number alone is meaningless without context: read vs write ratio (writes are more expensive), cache or not, data block size, controllers involved, storage type, RAID, tiering, sequential vs random.
- The most important parameter is latency in milliseconds. Rough VDI-era guide: 0-12ms good, 10-15ms acceptable, 15-20ms take action, 20-25ms shut it down.
- Bas's headline rule: 'a high number of IOPS is useless unless latency is low.'
- Three 'golden' parameters to demand from any storage vendor: latency (ms), read/write ratio, data block sizes used.
- Throughput (GB/sec) is not the same as IOPS; they overlap but differ.
- RAID carries a write penalty: a write isn't complete until both data and parity are written; reads are unaffected.
- On legacy HDDs, speed depends on RPM (5400/7200/10000/15000) and disk density (closer-packed data = shorter head travel = faster).

*Bron: blogpost 'The ultimate IOPS cheat sheet!' (2014-07-29), basvankaam.com.*

## Verwante notities

- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [Block vs file level storage, plainly](block-vs-file-storage.md)
- [Server 2012 R2 opened up cheaper VDI storage options](server-2012-r2-cheaper-vdi-storage.md)
- [Server 2012 R2 data dedup and the VDI separation rule](server-2012-r2-dedup-for-vdi.md)
- [VDI is more romantic on paper than in reality](vdi-romantic-vs-reality-position.md)
- [The five VDI workload phases and boot/logon storms](vdi-workload-phases-storms.md)
- [VMFS3 vs VMFS5 block and sub-block sizing](vmfs3-vmfs5-block-sizes.md)
