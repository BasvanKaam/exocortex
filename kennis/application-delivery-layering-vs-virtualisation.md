---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [application-delivery, app-layering, appdisks, appdna, virtualisation]
layer: rich
bron: inside-citrix-fma
---

# Application delivery: layering vs virtualisation, and AppDisks

Bas narrows application delivery to three ways but stresses there are far more flavours once you include virtualisation, layering and containerisation — he points readers to the Application Virtualization Smackdown whitepaper and rorymon.com.

AppDisks is Citrix's approach to application layering, manageable entirely from Studio, available across all XenDesktop editions (Advanced, Enterprise, Platinum) as of version 7.8. AppDNA integration with AppDisks is Platinum-only; when paired, AppDNA automatically checks whether your AppDisks (or other apps) are compatible with the target platform.

His nuance: application layering is not a direct replacement for application virtualisation — they go hand-in-hand, and in practice you'll likely use all three (base-image-installed, virtualised, and layered apps). Layering does not isolate applications; think of it as just another tool in the toolbox. And while a single master image is great, it's a utopia in most cases — don't go nuts, keep the number of images to a minimum. Less is more.

## Bron-citaten (NL, verbatim)

> Remember that, although a single master image is great to have, it is also a utopia in most cases. Just don't go nuts: keep the number of images to manage to a minimum. Less is more.
