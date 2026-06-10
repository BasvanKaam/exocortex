---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, licensing, flexera, license-server, netscaler]
layer: reference
bron: inside-citrix-fma
---

# Citrix licensing key facts (Flexera, capacity, NetScaler)

A few important facts about Citrix licensing infrastructure:

- Citrix Licensing relies on **Flexera** software (as do many other vendors).
- The license server is a relatively light role and can share a single physical or virtual server with other roles. A single license server can handle **over 10,000 continuous connections**.
- XenDesktop and XenApp are licensed through a central license server, but a **NetScaler** requires its license file to be uploaded directly to the device itself rather than residing on the license server.
- Getting licenses is a three-step process: **activate** (from the order confirmation email), **allocate** (select the number of users and generate the license file), and **download** (save and copy the file to the license server via the License Management Console).
- Citrix also runs a Trial Center for limited trial licenses; some are only available to registered Citrix partners.

## Verwante notities

- [Citrix license grace periods and supplemental grace period](citrix-license-grace-periods.md)
- [Citrix license types: user, device and concurrent](citrix-license-types-user-device-concurrent.md)
- [Citrix Licensing components and FlexNet](citrix-licensing-components-and-flexnet.md)
- [Citrix licensing: user, device and concurrent](citrix-licensing-models.md)
- [Startup license and the license checkout process](citrix-startup-license-and-checkout.md)
- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
