---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, rollback, boot-storm, reboot, disconnect-policy]
layer: rich
bron: inside-citrix-fma
---

# MCS rollbacks and reboot considerations (boot storms, disconnect policies)

Bas notes that MCS rollbacks (there is a rollback option in Studio specific to MCS) are treated like any other different image: the full copy-to-all-datastores process repeats. Note that if the previous image is still in use by some machines, no full copy is needed.

When an updated master VM is assigned, the VMs must be rebooted to use it. Bas flags the real-world snags from experience:
- Rebooting a couple of hundred VMs (or more) can negatively impact the underlying storage platform: a **boot storm**. Not something you want during work hours.
- Strict company policies on idle/disconnect sessions may forbid forced logoff, so you may have to reschedule your reboot plans. "Not that uncommon, trust me."
- It might interfere with other overnight processes.
- And, although off topic, all of this applies to Provisioning Services as well.

Key takeaway: give your idle and disconnect session policies some thought, it makes night-time rebooting easier depending on company policy.
