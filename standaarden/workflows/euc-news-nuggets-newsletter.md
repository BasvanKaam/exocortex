---
type: standaard
merk: bvk
domein: persoonlijk
status: actief
datum: 2026-06-19
tags: [workflow, content, nieuwsbrief, euc, linkedin]
---

# EUC News Nuggets: maandelijkse LinkedIn-nieuwsbrief

Een herhaalbaar recept voor Bas zijn maandelijkse EUC News Nuggets nieuwsbrief op LinkedIn: een gecureerd, geduid overzicht van wat er in de EUC-wereld tijdelijk misgaat, welke workaround er is, wat eraan komt, en welke deadlines naderen, over AVD, Windows 365, Intune en Windows.

## Cadans
Maandelijks, rond het midden van de maand. Begin een paar dagen ervoor met verzamelen en verifiëren, zodat publicatie rond de 15e kan.

## Wat het is (en niet is)
- Format: LinkedIn **newsletter-artikel** (long-form, gesectioneerd per platform), volle BvK-stem, Engels.
- De bron-ruggengraat is de lopende **EUC Nuggets Source Log** (Bas zijn cheat sheet/PDF: één regel per nugget, met bronlink). De PDF wordt **naast** de nieuwsbrief aangeboden als volledige referentie; het artikel hoeft dus niet elk detail te herhalen, het cureert en duidt.
- Dit is externe EUC-nieuwsduiding, **geen** vakinhoud voor het brein. De nuggets worden niet als `kennis/`-notities gedistilleerd. Alleen dit recept en eventuele voice-lessen horen in het brein.

## Stap 1: Verzamelen
1. Neem de nuggets van deze maand uit de lopende log.
2. Scan de officiële what-is-new / release-health / in-development pagina's (Microsoft Learn voor AVD, Windows 365, Intune, Windows release health) plus betrouwbare community-bronnen (kempeneers.eu, it-connect, BleepingComputer, EUC-bloggers) op verse known issues, fixes, previews en deadlines.
3. Mik op een hybride mix: de log als basis + een handvol hoogwaardige extra's per platform.

## Stap 2: Verifiëren (never invent, hard)
1. Verifieer elke dragende specific live tegen de officiële bron voordat je het stelt: datums, error codes, KB-nummers, versienummers, retirement-deadlines, prijswijzigingen. Conform `CLAUDE.md` en `standaarden/schrijfregels/nerdio-content-guard.md`.
2. Praktisch: draai een verify-pass met vier parallelle agents, één per platform (AVD / Windows 365 / Intune / Windows). Elke agent geeft per item TRUE/PARTLY/FALSE/OUTDATED + de precieze feiten + bron-URL, en stelt 1-2 geverifieerde extra's voor met verschillende inzichten.
3. **Named-expert-regel:** een met naam genoemde insider die het issue zelf vond, weegt zwaarder dan een neutrale doc-zin. Voorbeeld (juni 2026): de AVD Hybrid Arc-reboot is volgens Steve Downs (AVD Hybrid-team) een bug / race condition met fix in progress; de Microsoft deploy-doc beschrijft alleen de workaround neutraal. Volg de bron, niet de doc-toon, en crediteer de bron. Overcorrigeer Bas niet op basis van één doc.
4. Feed precisie-correcties terug in de log-PDF, zodat de referentie die je erbij aanbiedt ook klopt.

## Stap 3: Cureren en schrijven
Structuur:
- **Intro:** enthousiasme-led, de "spark" van deze maand (vaak een community-post; crediteer en tag de bron), dan kort wat de nieuwsbrief is, dan de doorverwijzing naar de PDF voor de volledige lijst.
- **Per platform een sectie** (AVD, Windows 365, Intune, Windows). Per item: wat het is, waarom het ertoe doet, Bas zijn take, en de workaround of datum. Geef voorrang aan wat lezers echt raakt; de rest staat in de PDF.
- **Datums om op te schrijven:** vouw deadlines en end-of-support-momenten samen tot een scanbare beat.
- **Outro ("How I use this"):** de log is levend, delen omdat de helft van de waarde zit in iemand die "ah, daarom" denkt voordat hij een middag verliest. Community-CTA: stuur een scherpere workaround of een ander inzicht, zo wordt de lijst beter. Sluit met "Until the next edition."

Voice-regels: volg `standaarden/voice/voice-profile.md` en `voice-corrections.md`. Volle BvK-stem, doorlopende komma-zinnen, geen em-dashes, geen AI-staccato (geen korte punch-zinnen als ritme-trucje), geen "clearly landed / trip over / humble"-achtige wendingen. Emoji alleen als flag. Crediteer peers met naam. Draai de banned-word scan voor je het toont.

## Stap 4: Uitleveren
- De nieuwsbrief als LinkedIn-artikel.
- De bijgewerkte EUC Nuggets Source Log (PDF) ernaast als volledige referentie.

## Harde regels (altijd)
- Never invent; verifieer elke technische claim live, flag bij twijfel.
- Geen em-dashes, nergens.
- Volle BvK-stem, banned-word scan voor publicatie.
- Crediteer bronnen en peers met naam; named-expert weegt zwaarder dan doc-toon.

## Verwante notities
- [Writing-pack generator (recept)](writing-pack-generator.md)
- [Brein-index (master)](../../kennis/index.md)
