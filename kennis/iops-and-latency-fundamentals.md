---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [iops, latency, storage, sizing, performance]
layer: rich
bron: inside-citrix-fma
---

# Bas on IOPS, latency and storage sizing

Bas's storage philosophy: 'Latency is king' — the less latency, the faster the infrastructure. A high IOPS number is useless unless latency is low; even SSDs that deliver huge IOPS still depend on latency, which tells you how long a single read/write request takes. There is no standard for measuring IOPS — too many factors influence it. A random IOPS number on its own means nothing: you must know reads vs writes, random vs sequential, single/multiple threads, block sizes, and above all the latency in milliseconds. Storage providers should give at least latency (ms), read/write ratio, and block sizes used in testing.

The average/Steady State alone is insufficient — also size for peak activity between boot and Steady State, and distinguish steady state, boot, logon, application-launch and logoff storms. Launching apps generates high read peaks and initial low writes, often causing an unrecognised application launch storm. Storage throughput is not the same as IOPS — throughput (GB/sec) matters for large data volumes. Reads are less intensive than writes and easier to cache. Don't forget CPU, memory and storage controllers as bottlenecks.

Practical fixes: if IOPS are limited, (pre-)boot machines at night and prevent users from rebooting machines themselves.

## Bron-citaten (NL, verbatim)

> Latency is king: the less you have, the faster your infrastructure will be!
>
> A high number of IOPS is useless unless latency is low!
