---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [iot, edge-computing, big-data, latency]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# IoT data placement: edge vs cloud by use-case

Where IoT data should be processed depends on data volume and latency sensitivity:

- **Workspace IoT** (e.g. booting a VDI when a user parks their car, or triggering login as they approach a thin client): small data volumes, data rarely leaves the building, no real-time need. Cloud-based third-party platforms are fine; a few seconds of delay goes unnoticed.
- **Industrial IoT** (a plant with thousands of sensors generating GBs of data): heat, friction, weight and micro/millisecond delays change the manufacturing outcome, so near-real-time processing is critical and **latency is one of the biggest enemies**. Process locally / as close to the source as possible; a third-party cloud only complicates things. This is where **edge computing** entered the datacenter.
- **Tracking and tracing** (sensors on containers/pallets sending GPS): local networks are useless, latency tolerance is high, so you want a low-power wide-range wireless network.

Durable principle: let the workload's data volume and latency tolerance, not fashion, pick edge vs cloud.

*Bron: blogpost 'All 'things' connected, the 'I' in the IoT - a closer look. Part two!' (2017-07-17), basvankaam.com.*

## Verwante notities

- [Take: big-data analytics is the real advantage of the cloud](cloud-analytics-real-advantage-stance.md)
- [LPWAN and LTE-IoT network families compared](lpwan-networks-sigfox-lora-nbiot-ltem.md)
- [LTE vs LPWAN trade-offs for IoT](lte-vs-lpwan-tradeoffs.md)
