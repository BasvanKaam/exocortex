---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [lte, lpwan, sigfox, iot-networking]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# LTE vs LPWAN trade-offs for IoT

LTE (cellular, higher-powered, measured in dB) has up to ~7x broader range than all low-power networks combined, higher max throughput (Kbps) and more connected devices. Downsides: it drains sensor batteries and underperforms for small, irregular data bursts.

LPWAN (Low Power Wide Area Network) conserves battery (10+ years) but offers far lower throughput and coverage, isn't available everywhere (still being built out across US/Europe c. 2017), and most are proprietary while LTE has the 3GPP standard.

The lines blur: LTE introduced low-power variants (LTE-M, NB-IoT) aimed at low power/bandwidth.

Spectrum note: licensed bands (LTE) give exclusive use, QoS and no interference for a fee; unlicensed ISM bands need no permission but are interference-prone (like home WLAN clashes on 2.4/5 GHz).

How the landscape looked in 2017; 5G was not yet available.

*Bron: blogpost 'All 'things' connected, the 'I' in the IoT - a closer look. Part two!' (2017-07-17), basvankaam.com.*

## Verwante notities

- [IoT data placement: edge vs cloud by use-case](iot-data-placement-edge-vs-cloud.md)
- [Variables that decide your IoT network choice](iot-network-selection-variables.md)
- [IoT networks won't be winner-take-all (2017 prediction)](iot-networks-not-mutually-exclusive.md)
- [IoT is a mindset shift; answer the business questions before the tech](iot-strategy-before-technology.md)
- [The three-block IoT architecture: Edge, Platform, Enterprise](iot-three-block-architecture.md)
- [Consumer IoT vs Industrial IoT (OT meets IT)](iot-vs-industrial-iot.md)
- [LPWAN and LTE-IoT network families compared](lpwan-networks-sigfox-lora-nbiot-ltem.md)
