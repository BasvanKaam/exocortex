---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [virtual-channels, priority, bandwidth, registry, qos]
layer: reference
bron: inside-citrix-fma
---

# ICA virtual channel priorities (0-3) and how to change them

Each virtual channel gets a default priority from 0 to 3; the lower the number, the higher the priority and the more bandwidth allowed. Example: printing defaults to priority 3 (lowest), so it gets less bandwidth than higher-priority channels like Audio and ThinWire (screen updates).

The four levels map to: very high (real-time, e.g. webcam), high (interactive: screen, keyboard, mouse), medium (bulk, e.g. client drive mapping) and low (background, e.g. printing).

Changing priorities manually is uncommon: giving more bandwidth to one channel takes it from another. If needed, edit `HKLM\System\CurrentControlSet\Control\Terminal Server\Wds\icawd\Priority`, which lists abbreviations (CTXCAM, CTXTWI, CTXFLASH, etc.) each with a number 0-3. Change the number to change priority. Always back up the key first.

Other ways to accelerate ICA traffic: Citrix policies (per user, per server, or whole Site) or a physical accelerator like Citrix CloudBridge (formerly Branch Repeater).
