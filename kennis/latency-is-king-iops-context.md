---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [storage, performance, iops, latency, sizing]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Latency is king, not raw IOPS

A high number of IOPS is useless unless latency is low. Even SSDs, which deliver huge IOPS versus traditional HDDs, still live or die by latency: latency tells you how long it takes to process a single read or write I/O request. There is no standard for measuring IOPS, too many factors influence it. The average (Steady State) is not enough either, you have to size for the peak activity measured between boot and Steady State. Storage throughput (GB/sec) is also not the same as IOPS, though they overlap. Practical levers Bas notes: pre-boot machines at night if IOPS are limited, stop users rebooting themselves, and watch for the application launch storm after logon (high read peaks). A durable storage-sizing principle that outlives any specific Citrix version.

*Bron: blogpost '100+ Citrix XenApp & XenDesktop FMA facts listed' (2017-04-11), basvankaam.com.*

## Verwante notities

- [IOPS, latency, and sizing storage for VDI workloads](iops-latency-and-sizing-storage-for-vdi.md)
