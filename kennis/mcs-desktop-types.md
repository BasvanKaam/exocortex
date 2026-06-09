---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, desktop-types, pooled, dedicated, catalog]
layer: reference
bron: inside-citrix-fma
---

# MCS desktop types: Pooled-Random, Pooled-Static, Dedicated

Using MCS you can provision three types of desktops (Catalog):

- **Pooled-Random**: a desktop is assigned randomly at logon. On logoff it becomes free for re-use and all changes are lost completely.
- **Pooled-Static**: a desktop is permanently assigned to a user at logon and stays with them after logoff. Any changes made are discarded during reboot/logoff.
- **Dedicated**: a desktop is permanently assigned to a user at logon and stays with them after logoff. Any changes made are saved to the VM no matter how many times it is rebooted or refreshed.
