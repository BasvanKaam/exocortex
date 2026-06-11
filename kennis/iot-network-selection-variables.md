---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [iot, networking, lpwan, lte]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Variables that decide your IoT network choice

Different 'things' produce different types and amounts of data, so the network choice depends on a long list of trade-offs:

- Where data lives: datacenter, edge, or sent to cloud for analysis.
- Distance between objects and how they connect.
- Communication frequency between sensor and platform.
- Autonomous decision-making -> needs continuous network access.
- Data volume (self-driving car vs sensor on a container).
- Latency tolerance and stability.
- Battery life: LTE's high dB extension drains sensor batteries; a dead battery means human intervention.
- Licensed vs unlicensed spectrum.
- Standards (3GPP/LTE) vs proprietary.
- Number of connections / scalability.
- Signal penetration through walls in dense buildings/cities.
- Setup/maintenance complexity, bandwidth (MHz), cost.

Durable framing: match the network to the use-case; tracking-and-tracing wants low-power, broad-range wireless, while local-edge processing needs little extra network.

*Bron: blogpost 'All 'things' connected, the 'I' in the IoT - a closer look. Part one!' (2017-07-10), basvankaam.com.*

## Verwante notities

- [LPWAN and LTE-IoT network families compared](lpwan-networks-sigfox-lora-nbiot-ltem.md)
- [LTE vs LPWAN trade-offs for IoT](lte-vs-lpwan-tradeoffs.md)
