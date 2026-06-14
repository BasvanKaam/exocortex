---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, remote-display-analyzer, rda, hdx, troubleshooting, community-tool, framehawk]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Remote Display Analyzer: detect and live-switch HDX codecs

How it worked then: the Remote Display Analyzer (RDA), by Bram Wolfs and Barry Schiffer (first shown at E2EVC Lisbon, Nov 2015), is a community tool that, launched inside an ICA/HDX session, instantly detects the current display mode, active encoder, visual quality, max FPS and other real-time stats, and shows only the info relevant to the detected mode. The free/lite version gives the real-time stats using a normal (non-admin) user account. The sponsored version lets you change display settings on the fly and live-switch between codecs (DCR, Thinwire, Framehawk included) without logging out, reconfiguring or rebooting, which Bas calls an industry first that even Citrix hadn't matched. Changes are made at ICA policy level (not codec level) and are supported by Citrix, but the advanced settings are for testing/experimenting only, not production.

*Bron: blogpost 'Presenting... The Remote Display Analyzer!' (2016-02-23), basvankaam.com.*

## Verwante notities

- [Take: Blast Extreme is an option, not a PCoIP killer](blast-extreme-not-a-pcoip-replacement.md)
- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [Framehawk and the Lightweight Framebuffer Protocol (LFP)](framehawk-lfp-protocol.md)
- [Linking infrastructure performance to employee productivity](infra-performance-vs-productivity.md)
- [RDA is an industry first that out-shipped Citrix itself](positie-rda-industry-first.md)
- [PowerShell: download the latest release asset from GitHub](powershell-download-latest-github-release.md)
- [Switching monitor resolution from a Stream Deck via Display Changer](stream-deck-resolution-switch-display-changer.md)
