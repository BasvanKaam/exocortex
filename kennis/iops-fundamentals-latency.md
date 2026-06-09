---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [iops, storage, latency, performance]
layer: rich
bron: inside-citrix-fma
---

# IOPS fundamentals: latency is king

IOPS = Input/Output Operations Per Second (a read or write). A disk capable of 100 IOPS can theoretically issue 100 read/write operations per second - but issuing is not the same as processing, because reading and writing data takes time. That delay is latency: how long a single I/O request takes. If a subsystem issues 100 IOPS but each takes 20ms (slow), it actually handles only ~50 operations per second.

Bas's latency rule of thumb:
- 0-12 ms: looking good (lower is better).
- 10-15 ms: still acceptable; users might notice a small delay.
- 15-20 ms: step up and take action; most users won't be happy.
- 20-25 ms: 'get your pen and paper out and shut it all down.'

FMA facts he emphasises: a high IOPS number is useless unless latency is low - even SSDs, which deliver huge IOPS vs HDDs, are bound by latency. And there is no standard for measuring IOPS; too many factors influence performance. Roughly, 2ms latency is comparable to a locally installed physical disk, while 20+ ms highly impacts performance.

## Bron-citaten (NL, verbatim)

> Latency is king: the less you have, the faster your infrastructure will be!
>
> 20 – 25 milliseconds – Get your pen and paper out and shut it all down.
