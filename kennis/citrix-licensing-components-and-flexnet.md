---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-licensing, flexnet, flexera, license-server, rds-licensing]
layer: reference
bron: inside-citrix-fma
---

# Citrix Licensing components and FlexNet

Licensing involves both Citrix (XenApp/XenDesktop) and Microsoft licenses (RDS, VDA - not the Citrix VDA, CDL, etc.). Bas notes some licensing details may no longer be 100% accurate due to changes over the prior two years.

Citrix relies on Flexera's FlexNet licensing software (formerly FlexNet Publisher / FLEXlm). FlexNet enforces software licensing and activation across on-premises, SaaS, cloud, virtualized and embedded applications.

Citrix Licensing components:
- License server: shares licenses across the network.
- License files: needed to license the product, stored on the License Server.
- License Administration Console: manages license files and the License Server.
- Web Services for Licensing: lets Studio, Director and the Licensing Administration PowerShell Snap-in communicate with the License Server (manage users, allocate/install licenses, display health, usage, alerts).
- Simple License Service: allocates and installs license files via a web page.
- Product-side settings in Citrix products associated with the License Server.

At least one license server is required. The role is light, so it can be co-hosted with other tasks, or even shared with other license servers such as Microsoft Licensing.

## Verwante notities

- [Citrix license types: user, device and concurrent](citrix-license-types-user-device-concurrent.md)
- [Citrix licensing key facts (Flexera, capacity, NetScaler)](citrix-licensing-key-facts-flexera.md)
- [Citrix licensing: user, device and concurrent](citrix-licensing-models.md)
- [Startup license and the license checkout process](citrix-startup-license-and-checkout.md)
- [How the license server reassigns user/device licenses](license-server-user-device-reassignment-logic.md)
- [Citrix Studio Configuration sub-nodes](studio-configuration-subnodes.md)
