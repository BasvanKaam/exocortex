---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [bas-checklist, printing, optimization, upd, policies, less-is-more]
layer: rich
bron: inside-citrix-fma
---

# Bas's checklist to speed up and clean up Citrix printing

Bas offers a practical checklist to improve and maintain Citrix printing:

- Apply true QoS through Multi-Stream ICA; optionally give the ICA virtual print channel a higher priority (careful with this).
- Use the UPD and configure 'Universal printing image compression limit' (max quality / min compression for images); use the UPS for additional compression/QoS and configure 'Universal printing print quality limit' (max dpi).
- Allocate/limit/control print bandwidth via policies (per user or whole Site): 'Printer redirection bandwidth limit percent' (% of overall bandwidth) and 'Printer redirection bandwidth limit' (kbps), freeing HDX bandwidth for video, keystrokes and mouse.
- Configure session (network) printers, on faster networks only.
- Driver matching: the server tries to match the client driver (same name AND version); if not found it tries a native Windows driver, then falls back to the UPD (must be enabled). Configure 'Automatic installation of inbox printer drivers' to control this.
- Use 'printer driver mapping compatibility' when client and server drivers are named differently but equivalent; supports wildcards (e.g. HP* forces all HP printers to one driver), whitelisting, banning a driver with 'Do not create', steering printers to the UPD, and reducing total drivers/admin overhead.
- The Universal Printer eliminates printer enumeration at logon; configure image quality, heavyweight compression (bandwidth reduction without quality loss), and image/font caching.
- Use the client printing pathway where it makes sense, even on fast internal networks, since ICA can help performance.
- 'Printer properties retention' policy controls where preferences are stored (client device by default, else the user profile); Citrix advises keeping defaults.
- Map the default client printer only; mapping all known printers 'can take forever.'
- Avoid upgrading print drivers: uninstall the old and install the new, keeping machines clean.
- Limit the number of installed drivers ('less is more!'); use signed drivers exclusively and always thoroughly test the architecture 'no matter how convinced you may be that it will work.'
- The simpler the driver, the less traffic; use vendor drivers only when specific functionality is needed.
- Apply print driver isolation where it makes sense (it costs CPU/memory).
- Only use version 3 and 4 drivers; match the print server OS to the XenApp server OS; use Citrix Director for real-time printing bandwidth info; check the Citrix Ready guide for supported models.

FMA fact (his caution): it isn't just about bandwidth; check for congestion and latency too. He also notes this all applies to both XenApp and XenDesktop and most isn't IMA- or FMA-specific.

## Bron-citaten (NL, verbatim)

> Limit the number of print drivers installed – less is more!
>
> always thoroughly test your print architecture set-up, no matter how convinced you may be that it will work
