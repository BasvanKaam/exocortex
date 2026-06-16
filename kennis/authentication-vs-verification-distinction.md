---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [authentication, verification, brokering, definition, fma-fact, storefront, security]
layer: rich
bron: inside-citrix-fma
---

# Bas's distinction: authentication versus verification

Bas calls out a precise distinction he uses throughout the book (an FMA fact): authentication and verification are not the same thing, and he is deliberate about it because people often blur the two terms.

- Authentication is making sure somebody is who he or she claims to be.
- Verification (he also calls it validation) is finding out which resources are assigned to the user, i.e. their permissions. Those resources are then displayed in the user's store, ready for subscription.

User authentication and resource enumeration go hand-in-hand. During login the Delivery Controller plays a role in both, a process also called connection brokering. Bas flags this distinction explicitly so readers notice when he uses each term.

## Bron-citaten (NL, verbatim)

> Note how I mention user authentication and user validation. There is a difference. Authentication is to make sure that somebody is who he or she claims to be. Verification is done to find out which resources are assigned (permissions) to the user.

> Note how I mention user authentication and user validation. There is a distinct difference.

## Verwante notities

- [Bas's key takeaways on the user login process](bas-key-takeaways-user-login-process.md)
- [Broker Service: XML, STA and the Principal Broker](broker-service-xml-sta-principal.md)
- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [Authentication vs verification are two distinct steps](fma-authentication-vs-verification.md)
- [XenMobile PIN + certificate as two-factor auth](xenmobile-pin-certificate-2fa.md)
