---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [high-availability, best-practice, resilience, design]
layer: rich
bron: inside-citrix-fma
---

# Bas's 'one is none' rule for resilience

Bas's guiding redundancy maxim: your environment is only as strong as its weakest link, so apply the 'one is none' rule wherever and whenever it makes sense. A single instance of any critical component is effectively no resilience at all.

He applies it across the FMA: deploy at least two Delivery Controllers per Site (and per Zone where possible), make PVS infrastructure highly available, and pair NetScalers (the rule applies to NetScalers as well). It is a recurring design principle throughout the book rather than a one-off remark.

## Bron-citaten (NL, verbatim)

> Your environment is as strong as its weakest link. Make sure to apply the 'one is none' rule wherever and whenever it makes sense.
>
> Remember the one is none rule? Well, it applies to NetScalers as well.
