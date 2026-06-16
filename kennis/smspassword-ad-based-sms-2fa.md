---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [authentication, 2fa, sms, active-directory, netscaler, radius]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# SMSPassword: on-prem SMS 2FA that leans on Active Directory for HA

How it worked then (2016): SMSPassword was an on-premises SMS-based two-factor authentication product. Design points Bas highlighted:
- Integrates with existing AD with no schema changes or extra user attributes, and uses AD as its store, so no separate database. Because AD is redundant by nature, database HA comes for free.
- Deployed 100% on-site, giving the admin full control. Installs as a small portable .exe (a few MB), no extra Windows roles, and can sit on existing StoreFront servers.
- Acts as a RADIUS server supported by Citrix NetScaler, Palo Alto, F5, Juniper, Barracuda, Check Point, Cisco, VMware, SharePoint and more.
- Works with any phone that supports SMS (no app, no smartphone needed); also offered time-based tokens via an iOS/Android app for no-signal situations, with a Windows Phone app then on the roadmap.
- Scales horizontally: multiple SMSPassword servers and SMS dispatch modems behind a load balancer (e.g. NetScaler) with heartbeat monitors for HA. Lifetime licenses in a flexible, reassignable pool.

*Bron: blogpost 'Two factor (SMS) authentication -- done right with SMSPassword!' (2016-10-04), basvankaam.com.*

## Verwante notities

- [XenMobile PIN + certificate as two-factor auth](xenmobile-pin-certificate-2fa.md)
