---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [bas-tip, printing, client-pathway, wan, branch-office]
layer: rich
bron: inside-citrix-fma
---

# Bas: forcing the client printing pathway (and its exception)

Bas explains a scenario where, despite a print server being present, you'd prefer the client printing pathway: when the XenApp server is in the datacenter and the print server is near the users in a branch office. Since XenApp-to-print-server traffic is unmanaged/uncompressed, this WAN-separated setup is risky.

The fix: force the client printing pathway by disabling the 'Direct connection to print server' policy. Then print output is first sent back to the client over ICA (compressed), then handed to the nearby print server and physical device, all close together: a much more efficient approach.

The exception to the rule (and Bas notes 'there always is'): if the print server is back in the datacenter, forcing the client printing pathway makes things worse. The output goes from XenApp to the client over ICA (compressed), then must traverse the WAN back to the datacenter print server uncompressed, then the rendered job goes back to the branch-office device, again uncompressed. He warns to avoid this setup.
