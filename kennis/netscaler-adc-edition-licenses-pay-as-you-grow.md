---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, licensing, burst-pack, universal-license]
layer: reference
bron: inside-citrix-fma
---

# NetScaler edition licenses and Pay-as-you-Grow

Every ADC NetScaler (physical or virtual) takes one of three **edition (platform) licenses**: Standard, Enterprise or Platinum. Each unlocks more functionality on upload, following the **Pay-as-you-Grow** model — e.g. start on Standard, later upload an Enterprise license to unlock a feature like dynamic content caching, no hardware change required. Every normal ADC license already includes Gateway functionality by default; no additional license needed.

Other license types: Internal, Partner use, Demo, Evaluation, Express, Developer and VPX. SDX appliances require licenses for each physical appliance and each virtual instance.

The **Universal license** (a.k.a. Concurrent User license / CCU) is optional and enables the Gateway/Enterprise appliance to support a set number of concurrent users for features like full SSL VPNs, Smart Access Endpoint Analysis, Clientless Access and Micro VPNs (XenMobile). Total concurrent user sessions on a Gateway vServer cannot exceed the count in the universal license.

**Burst Packs** temporarily increase network throughput to absorb sudden traffic spikes without buying new hardware. Maintenance contracts come in gold/silver/bronze (3/2/1 years of support). Buying order: pick the physical/virtual model, then the edition license, then a maintenance contract.
