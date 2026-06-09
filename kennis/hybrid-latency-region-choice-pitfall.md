---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [hybrid, latency, region, design, war-story]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Hybrid Latency and the Region-Choice Pitfall

Bas shares a hard-won design lesson. In a hybrid model, the design of the environment has big performance impact. Internet is everywhere and users can connect from almost any device/location, but the connection from your chosen cloud environment to a local datacenter is another story.

If you split systems — e.g. publishing a web portal in your cloud (desktop) environment while the associated databases stay in your own datacenter — you can get latency problems and slow processing/retrieval of information. Your choice of cloud region can play a role here, something Bas says he has unfortunately encountered more than once in practice. His maxim applies: 'goedkoop is duurkoop' (cheap turns out expensive), since cloud service costs differ per region. Usually a design decision or a budget decision lies at the root of it.
