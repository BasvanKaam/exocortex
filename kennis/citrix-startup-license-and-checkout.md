---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, licensing, license-server, fma]
layer: reference
bron: inside-citrix-fma
---

# Startup license and the license checkout process

Each time a Citrix product starts it checks out a **startup license**, which enables the product to maintain a continuous connection to the License Server. When a user connects, the Citrix product requests to check out a license from the License Server on behalf of the user or device; once successfully checked out, the user can use the product. The whole assignment process (concurrent or not) is also called the checking in and checking out of **license tokens**.

When user/device licenses are issued, a token is applied for both a XenDesktop and a XenApp license token even if you only connect to one — they are always issued in pairs.

Within the FMA, the **Delivery Controller(s)** handle license checkout and communication with the license server (in the older IMA this was the responsibility of the Session Hosts). When licenses are allocated they are 'bound' to the license server, identified by its local hostname, which is case sensitive.

## Verwante notities

- [Citrix license grace periods and supplemental grace period](citrix-license-grace-periods.md)
- [Citrix license types: user, device and concurrent](citrix-license-types-user-device-concurrent.md)
- [Citrix Licensing components and FlexNet](citrix-licensing-components-and-flexnet.md)
- [Citrix licensing key facts (Flexera, capacity, NetScaler)](citrix-licensing-key-facts-flexera.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [How the license server reassigns user/device licenses](license-server-user-device-reassignment-logic.md)
