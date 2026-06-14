---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, netscaler, 10.5, ica-proxy, licensing, access-gateway]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# NetScaler 10.5 made ICA proxy built-in and unlimited

How it changed with NetScaler 10.5 (2014):

- Before 10.5: to do ICA proxy you bought a separate Access Gateway platform license that raised ICA users to 10,000 (default was 0), plus optionally a universal license.
- With 10.5: the ICA-proxy / Access Gateway platform license is built into every edition (NSGW, Standard, Enterprise, Platinum) by default, and the ICA user count is set to unlimited. You can no longer buy the separate platform license.
- The universal license stays optional and separate (still needed for SmartAccess, Micro VPN, full SSL VPN).
- 'Unlimited' is a licensing statement, not a hardware one: a VPX still tops out around 1500 concurrent ICA connections; physical MPX models handle ~10,000 to 35,000 depending on model.

Bas framed this as Citrix simplifying licensing without forcing customers to spend more.

*Bron: blogpost 'Citrix NetScaler (10.5) licensing. What's new with Access Gateway!' (2014-07-01), basvankaam.com.*

## Verwante notities

- [Credit to Citrix for simplifying NetScaler licensing without a price grab](citrix-simplifying-licensing-praise.md)
- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler ADC vs Gateway: same box, different license](netscaler-adc-vs-gateway-licensing.md)
- [NetScaler HDX Proxy announced to replace the Secure Gateway (Synergy 2016)](netscaler-hdx-proxy-replaces-secure-gateway.md)
- [NetScaler platforms, editions and HA](netscaler-platforms-and-licensing.md)
