---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [xenmobile, mdm, netscaler, security, positie]
bron: basvankaam-blog
---

# Getting the XenMobile MDM server out of the DMZ was overdue and underdiscussed

In January 2014 Bas welcomes Citrix finally shipping the XenMobile Device Manager SSL Offload patch for NetScaler (from XenMobile MDM 8.6.1, released December 2013). Before this, the MDM server had to live in the DMZ because it authenticated, decrypted and encrypted all SSL traffic itself, both a resource burden and an insecure placement. Now NetScaler can do the SSL work and the MDM server can sit on the more secure internal network.

His stance includes mild surprise that nobody was talking about it: "for some reason I haven't read or heard a thing about it. Perhaps XenMobile isn't as popular as I thought or people just don't mind putting their MDM machines in their DMZ's, I know I would [mind]." The post also doubles as Bas openly stepping outside his comfort zone: he admits he was "never really… a networking kind of guy" and uses the XenMobile work as the push to finally learn NetScaler. A good example of him publicly learning a weak area.

*Bron: blogpost 'NetScaler SSL Offloading for XenMobile MDM... Finally!' (2014-01-27), basvankaam.com.*

## Verwante notities

- [If traffic is inspected and users authenticated, the DMZ is at least as safe as the LAN](dmz-not-automatically-safer-than-lan.md)
- [A framework for deciding DMZ vs internal LAN server placement](dmz-placement-decision-framework.md)
- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [MDM enrollment binds both the device and the user (durable concept)](mdm-enrollment-device-then-user.md)
- [NetScaler SSL offload, wildcard and SAN certs](netscaler-ssl-offload-and-cert-types.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [XenMobile MDX: Vault, Interapp and Access](xenmobile-mdx-vault-interapp-access.md)
- [XenMobile MDM moved off the DMZ via NetScaler SSL offloading](xenmobile-ssl-offloading-netscaler.md)
