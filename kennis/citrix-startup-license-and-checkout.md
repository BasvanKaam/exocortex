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
