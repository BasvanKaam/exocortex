---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [exchange, mail, message-size, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Exchange Message Size Limit Precedence

How message-size limits stacked in Exchange. Limits exist at several levels: organization send/receive, per-mailbox send and receive, send connector, and receive connector. A message must pass every applicable limit; the most restrictive wins.

Bas's worked example: org limit 20MB; Barbara's mailbox send/receive 40MB; Mark's mailbox receive 40MB; send and receive connectors each 20MB. Resulting scenarios:

1. Barbara (40MB) → Mark: passes Barbara's send limit, OK.
2. Barbara (40MB) → Dean: passes Barbara's send limit but blocked by the 20MB org limit.
3. Barbara (40MB) → external: passes her send limit but blocked by org limits.
4. Barbara (20MB) → external: passes send limit, org limits, and send connector limit → sent.
5. Inbound (20MB): passes receive connector, org limits, and Barbara's receive limit → OK.

Key takeaway: a generous per-mailbox limit does not override a tighter organization or connector limit.

*Bron: Core Knowledge doc 'Order of Precedence Mail Limit Sizes Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix policy precedence: IMA vs Citrix AD vs normal AD policies](citrix-policy-precedence-ima-ad.md)
- [DNS resource record types](dns-resource-record-types.md)
- [How share and NTFS permissions combine](share-vs-ntfs-permission-combination.md)
