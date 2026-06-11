---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [sigfox, lora, nb-iot, lte-m, lpwan]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# LPWAN and LTE-IoT network families compared

A c.2017 map of the main IoT connectivity options:

- **Sigfox**: first modern LPWAN (France, 2009). Extreme-low-bandwidth, ultra-low-energy, proprietary open standard, IoT-only network. 868 MHz in Europe, 900 MHz in the USA; broadest coverage in Europe, still building out in the US.
- **LoRa / LoRaWAN**: 'Long Range', 0.3-50 Kbit/s. LoRa is the proprietary physical layer (Semtech chips); LoRaWAN is the networking protocol on top. Uses an Adaptive Data Rate (ADR) algorithm where the network server tunes each sensor's data rate for battery/capacity. The Netherlands had the first nationwide LoRa network (KPN, June 2016). Key advantage: can also be deployed as private networks.
- **NB-IoT**: 3GPP Rel.13, DSSS modulation, doesn't use the LTE spectrum directly but can reuse LTE base stations (in-band or guard-bands) or repurposed 200 kHz GSM bands. No gateways needed; cheaper chips. Backed by Huawei, Ericsson, Qualcomm, Vodafone.
- **LTE-M (Cat-M / LTE-MTC)**: 3GPP Rel.13, co-exists with LTE via a software upgrade, more secure, higher data rates, ~10 years battery on a 5WH battery; often seen as superior to NB-IoT.
- **LTE Cat 1**: 3GPP Rel.8, only full-LTE IoT standard then, candidate to replace 3G as it 'sunsets'.
- **LTE Cat 0**: 3GPP Rel.12, designed for IoT, complexity reduced >50% (single antenna, half-duplex); foundation for LTE-M, candidate to replace 2G.

How the IoT connectivity landscape looked in 2017.

*Bron: blogpost 'All 'things' connected, the 'I' in the IoT - a closer look. Part three!' (2017-08-15), basvankaam.com.*

## Verwante notities

- [Industrial IoT will be the biggest sub-vertical (2017 call)](iiot-the-next-big-thing-2017.md)
- [IoT data placement: edge vs cloud by use-case](iot-data-placement-edge-vs-cloud.md)
- [Variables that decide your IoT network choice](iot-network-selection-variables.md)
- [IoT networks won't be winner-take-all (2017 prediction)](iot-networks-not-mutually-exclusive.md)
- [The three-block IoT architecture: Edge, Platform, Enterprise](iot-three-block-architecture.md)
- [LTE vs LPWAN trade-offs for IoT](lte-vs-lpwan-tradeoffs.md)
