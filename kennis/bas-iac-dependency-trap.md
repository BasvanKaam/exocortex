---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [iac, bas-experience, vendor-lock-in, partner, security-updates]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Bas's War Story: The IaC Dependency Trap

A hard-won Bas observation: IaC offers huge benefits but is very hard to truly master, something he runs into regularly with clients. A common failure pattern he describes:

1. A client works with a partner who sets everything up via IaC, and life is good.
2. The partner slowly fades out of the picture, and then the misery begins ("dan begint de ellende").
3. The local IT team has no idea how to maintain the code or make changes; when something breaks they usually can't troubleshoot it. Adding new features or modifying existing code is hard, and the backlog grows ever longer.
4. The partner re-enters the picture, and a strong (and often costly) dependency has been created.

Even with good handover and documentation, Bas argues the material is simply too hard to master well that way. He has also seen cases where the partner did NOT return and the internal team did what it could; after a few months nearly all systems had fallen behind on security updates, again an undesirable situation. His verdict: relying on a reliable partner can be a deliberate, legitimate choice, but think it through carefully. "Zint voor ge begint."

## Bron-citaten (NL, verbatim)

> De partner verdwijnt langzaam uit beeld en dan begint de ellende.
>
> “Zint voor ge begint.”

## Verwante notities

- [Bas: IaC Creates Dangerous Key-Person Dependency](bas-iac-key-person-risk.md)
- [Bas on handover: 'simple is better'](bas-on-simplicity-handover-checklist.md)
- [The human factor: loss of control and trust](bas-on-the-human-factor-and-loss-of-control.md)
- [Infrastructure as Code (IaC) and Its Benefits](infrastructure-as-code-basics.md)
- [No universal Cloud standard, and the vendor lock-in problem](no-universal-cloud-standard-vendor-lock-in.md)
- [Handling Resistance and Fear of the Unknown](resistance-and-fear-of-the-unknown.md)
- [Bas: Saying You're Cloud-Native vs Actually Being It](saying-cloud-native-vs-being-it.md)
