---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [iot, architecture, edge, big-data, api, security]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# The three-block IoT architecture: Edge, Platform, Enterprise

Bas frames an IoT architecture as three building blocks (partly based on a Gartner model):

- The Edge: sensors, gateways, simple and smart IoT devices. Mostly hardware. Security concerns: endpoint security, encrypted communication to/from the platform, maintenance and update cycles, and devices often physically outside IT's direct control.
- The IoT platform: handles authentication, event processing, protocols, logical workflows and Edge device management; mostly platform-agnostic. It is built from many components (storage, databases, analytics, network, auth) each needing securing. Big Data / data warehousing sits here.
- The Enterprise: data warehousing, application services, data visualization, and crucially API integration to tie it together, on top of mostly existing, already-secured infrastructure.

Breaking the design into these three blocks is also his recommended starting point for a security assessment. The human factor (security awareness, mishandled data) cuts across all three. Durable conceptual framing; the named platforms below it are dated.

*Bron: blogpost 'Defining your IoT strategy - first things first!' (2017-02-06), basvankaam.com.*

## Verwante notities

- [Citrix Octoblu: an everything-is-a-node IoT platform](citrix-octoblu-architecture.md)
- [Take: big-data analytics is the real advantage of the cloud](cloud-analytics-real-advantage-stance.md)
- [The Connected Cow: an IoT + cloud big-data use case](connected-cow-iot-bigdata-usecase.md)
- [Industrial IoT will be the biggest sub-vertical (2017 call)](iiot-the-next-big-thing-2017.md)
- [LPWAN and LTE-IoT network families compared](lpwan-networks-sigfox-lora-nbiot-ltem.md)
- [LTE vs LPWAN trade-offs for IoT](lte-vs-lpwan-tradeoffs.md)
