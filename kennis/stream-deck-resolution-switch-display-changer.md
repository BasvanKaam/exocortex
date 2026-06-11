---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [stream-deck, display-changer, resolution, command-line, presenting]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Switching monitor resolution from a Stream Deck via Display Changer

How it worked then (Dec 2020): to switch a widescreen monitor between its native 3440x1440 and a presentation-friendly 2560x1440 from a Stream Deck button, Bas used 12noon "Display Changer" (free for personal use), which changes display resolution (optionally runs a program, then restores settings) and can rearrange monitors in a multi-monitor setup.

Steps:
1. Install Display Changer; default path `C:\Program Files (x86)\12noon Display Changer\dc.exe`.
2. Identify monitors with `dc.exe -listmonitors`.
3. Change resolution with: `dc.exe -monitor="\\.\DISPLAY2" -width=xxxx -height=xxxx`.
4. Test from a command prompt first, then in the Stream Deck software add an "Open" action, paste the command line into the App/File field, and assign a custom icon.

Bas made his own icons (e.g. a "2560" and a "3440" button) by drawing 1" squares in PowerPoint and cutting them out as PNGs with Snagit. The durable idea: bind a console command to a hardware key to make a repetitive presentation chore a one-press action.

*Bron: blogpost 'Using the Elgato Stream Deck to change your screen resolution' (2020-12-27), basvankaam.com.*

## Verwante notities

- [Bas's teaching philosophy: action and presenting beat passive reading](bas-teaching-philosophy-action-and-presenting.md)
- [Start cheap, have fun, upgrade later: his take on entering sim racing](console-over-pc-sim-racing-pragmatism.md)
- [Choosing a screen for console sim racing: what actually matters](console-sim-racing-screen-choices.md)
- [Remote Display Analyzer: detect and live-switch HDX codecs](remote-display-analyzer-tool.md)
- [WFH is not going away anytime soon](wfh-is-here-to-stay-2020.md)
- [Bas's 2020 WFH / streaming kit-list](wfh-setup-kitlist-2020.md)
