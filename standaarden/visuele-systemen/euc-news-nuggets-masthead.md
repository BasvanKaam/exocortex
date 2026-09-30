---
type: standaard
merk: bvk
domein: persoonlijk
status: actief
datum: 2026-06-25
tags: [visueel, header, masthead, nieuwsbrief, euc, linkedin]
---

# EUC News Nuggets: header / masthead-systeem

Het vaste visuele systeem voor de header-afbeelding bovenaan elke EUC News Nuggets editie (LinkedIn-nieuwsbrief / artikel-top). Afgeleid uit Bas zijn eigen edities (NO. 004, 005, 006). Stijl: **vintage editorial krantenkop**. Per editie wisselt alleen de illustratie en de dek; de bovenkant blijft identiek.

> Let op: dit is een ander systeem dan de [BvK PDF editorial skin](bvk-pdf-design-system.md) (coffee/cream, Bowlby/Yeseva, voor microlearning-lessen) en de Nerdio-carousel-skin. Niet door elkaar halen. Deze masthead is specifiek voor de nieuwsbrief-header.

## Formaat
- 1280×720 (16:9), de LinkedIn newsletter cover-maat.

## Exacte afmetingen (vastgelegd 2026-07-14, geijkt op No. 010)
Alle waarden in 1x (1280×720). Render op 2x (2560×1440) supersampled voor scherpte, daarna eventueel terugschalen naar 1280×720.

- **Canvas:** 1280×720. Achtergrond donkere editie `#1b2230`.
- **Zijmarges:** 132px links en rechts (contentbreedte 132–1148). Zelfde marge overal.
- **Top-rule:** y=70, dik 2px, cream `#ece2cd`, van 132 tot 1148.
- **Kicker-rij:** Archivo 600, 20px, tracked .16em, cream, verticaal midden y≈100. Links `EUC MICROLEARNING`, midden `VOL. I · NO. 0XX`, rechts `FREE TO READ & LISTEN`.
- **Masthead-titel `EUC News Nuggets`:** Playfair Display 800, 116px, `#efe7d4`, gecentreerd. **Regel: gelijke ruimte boven en onder tussen de tekst en de strepen**, gemeten op cap-hoogte en basislijn (niet op de g-staarten): 63px van cap-top tot de top-rule, 63px van de basislijn tot de dubbele rule. (In het script: `DELTA_BELOW=0`, positionering op cap/asc-metrics.)
- **Dubbele rule:** y=280, dik 5px + dun 2px met 5px tussenruimte, cream.
- **Rode dek/eyebrow:** Archivo 700, 21px, tracked .28em, brick `#d4512a`, gecentreerd, y≈356.
- **Headline (per editie):** Playfair Display Italic 800, 60px, cream, één mustard `#FEA712` pop-woord, gecentreerd, y≈430.
- **Standfirst (optioneel):** Georgia italic 24px, muted `#b9b096`, gecentreerd, y≈524.
- **Footer-rule:** y=628, 2px, cream op ~55%.
- **Footer:** links `bvk.` (Archivo 800, 34px, cream, oranje `#E76219` punt), rechts de tagline (Georgia italic 22px, `#d6ccb4`). Bij No. 010 getrimd tot `Short reads.`
- **Fonts:** Playfair Display en Archivo als variable fonts van Google Fonts (`ofl/...`), Georgia lokaal (`C:\Windows\Fonts\georgiai.ttf`).

**Render-pijplijn (belangrijk):** headless Chrome starten is in deze omgeving geblokkeerd, dus renderen gaat met **Python + Pillow** direct naar PNG (variable-font-assen via `set_variation_by_axes`, tracked caps via een per-glyph teken-loop). Script: `.tmp_euc/render_no010_masthead.py`. Waarden bovenin het script (`TOP_RULE_Y`, `DBL_Y`, `DELTA_BELOW`, dek, headline, editienummer) aanpassen en opnieuw draaien.

## Vaste elementen (elke editie hetzelfde — "de bovenkant in stand houden")
- **Top-balk**, tracked caps, dunne rule erboven en eronder:
  - links: `EUC MICROLEARNING`
  - midden: `VOL. I · NO. 00X` (volgnummer telt op per editie)
  - rechts: `FREE TO READ & LISTEN`
- **Masthead-titel**: *EUC News Nuggets* in **Playfair Display** (weight 800), een high-contrast didone display-serif. Gestandaardiseerd op 2026-06-25: de originele headers (t/m NO. 006) waren Claude-artifacts waarvan alleen de PNG bewaard bleef, de bronfont was niet te achterhalen. Playfair matcht de oude masthead vrijwel exact (de karakteristieke `g`, de dik/dun-contrasten) en is voortaan de vaste font. Top-balk + kicker in een grotesque (Archivo); de stamp in Archivo Black.
- **Dubbele horizontale rule** direct onder de titel (klassieke masthead: dik + dun).
- **Tagline** (italic serif): *Short reads. Short listens. No fluff.* — variant op de BvK-tagline "Short reads. Sharp takes. No fluff."; hier dekt "reads / listens" bewust de cheat sheets én de podcasts.
- **`bvk.`** woordmerk, linksonder, met rode/oranje punt.

## Variabele elementen (per editie)
- **Themed illustratie**: vintage ge-etste plaat of dramatische foto die het thema van de maand verbeeldt. Voorbeelden: krantenjongen op fiets (NO. 006), rij parkeermeters met rode vlaggetjes = aflopende services (NO. 005), figuur tussen twee lichtpaden, dark/near-black achtergrond (NO. 004).
- **Editie-band** (optioneel, brick-rood, helemaal bovenaan): bijv. `KNOWN ISSUES EDITION`.
- **Rode kicker + italic dek** (optioneel): bijv. `KNOWN ISSUES` + *"What broke this month across AVD, Windows 365, Intune and Windows, and how to work around it."* Of een tracked-caps dek zoals `12 (CLOUD) SERVICES ABOUT TO EXPIRE` (NO. 005).
- **Rubber-stamp** (optioneel, brick-rood, schuin): bijv. `STOP THE PRESSES`.
- **Achtergrond**: standaard creme/off-white papier; near-black voor zware/moody thema's.

## Kleur
- Papier: warm creme / off-white.
- Inkt: bijna-zwart.
- Accent: brick/rust-rood (banden, stamps, kickers, de punt van `bvk.`).
- Dark-editie: near-black achtergrond, creme titel en inkt.

## Toepassing op een nieuwe editie
1. Houd de hele bovenkant gelijk; verhoog alleen `NO. 00X`.
2. Kies één thema-illustratie in de etch-stijl (illustratie genereert Bas zelf, bijv. Midjourney/DALL·E).
3. Schrijf een dek/kicker die het thema duidt; optioneel een editie-band en stamp in rood.
4. Voice-regels gelden voor alle tekst op de header: volle BvK-stem, geen em-dashes, banned-word scan. Zie [voice-profile](../voice/voice-profile.md) en [voice-corrections](../voice/voice-corrections.md).

## Verwante notities
- [EUC News Nuggets nieuwsbrief-recept (workflow)](../workflows/euc-news-nuggets-newsletter.md)
- [BvK PDF editorial design system](bvk-pdf-design-system.md)
- [EUC News Nuggets platform pivot](../../kennis/eucnewsnuggets-platform-pivot.md)
