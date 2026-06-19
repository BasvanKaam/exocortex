---
type: standaard
merk: bvk
domein: persoonlijk
status: actief
datum: 2026-06-19
tags: [workflow, schrijven, content, voice, posities]
---

# Writing-pack generator

Een herhaalbaar recept om van een onderwerp een schrijf-klare bundel te maken: de relevante posities, de feiten, en de voice-guardrails op een rij, zodat een post op Bas zijn echte standpunten en stem staat, snel, en zonder iets te verzinnen.

Trigger: Bas zegt iets als "writing-pack over X", "schrijf een post over X", of "maak een pack voor X". Output is OF alleen de pack (als hij die eerst wil zien), OF de pack plus een eerste draft.

## Waarom dit bestaat
Het brein is de bron. Een goede post komt niet uit algemene kennis maar uit Bas zijn gedistilleerde posities + de voice-laag. Dit recept dwingt die volgorde af: eerst standpunt en feit ophalen, dan pas schrijven. Het voorkomt generieke AI-content en feitfouten, en het houdt de harde regels (never invent, geen em-dashes, juiste register, banned-word scan) in het proces.

## Stap 0: Scope (alleen als onduidelijk)
Bepaal, kort: het onderwerp/de invalshoek, het kanaal (LinkedIn, blog, carousel, talk, podcast), de taal (Engels default; Nederlands alleen voor het Academy/finance-kanaal, zie `standaarden/schrijfregels/output-taal-engels.md`), en de lengte. Niet doorvragen als het uit de opdracht al blijkt; kies anders het meest logische en zeg welke aanname je doet.

## Stap 1: Posities ophalen (de ruggengraat)
1. Open `kennis/positie-digest.md` en pak het thema-cluster dat het onderwerp raakt.
2. Vul aan via de domein-indexen (sectie Posities) of `grep` in `kennis/` op het onderwerp, voor stances die niet in de digest staan.
3. Kies de 3 tot 6 sterkste, meest relevante posities. Lees de notitie zelf (niet alleen de titel), pak de kern in één zin, en noteer de bestandsnaam als bron. Geef voorrang aan `layer: rich`.
Als er geen positie is op dit onderwerp: zeg dat. Dan is dit geen post-vanuit-fundament maar een nieuw standpunt dat Bas eerst zelf moet vormen (kandidaat voor een interview-vraag of een nieuwe positie-notitie).

## Stap 2: Feiten ophalen (en verifiëren)
1. `grep` in `kennis/` naar relevante reference-feiten, cijfers, namen.
2. Markeer elke technische claim met zijn bron-notitie.
3. NEVER INVENT. Voor Nerdio- en productclaims geldt de harde regel uit `CLAUDE.md` en `standaarden/schrijfregels/nerdio-content-guard.md`: verifieer live tegen de officiële bron (NME/NMM Help, Microsoft Learn) voordat je het stelt. Twijfel je over een feit dat niet in het brein staat? Flag het of verifieer het; gok niet.

## Stap 3: Voice ophalen
1. Lees `standaarden/voice/voice-profile.md` en `standaarden/voice/voice-corrections.md` (verplicht voor alles in BvK-stem).
2. Kies het register via de register-dial: volle BvK-stem voor LinkedIn/blog/carousel/talks en alles dat hij over Nerdio publiceert; Nerdio corporate-warmed voor officiële Docebo-lessen/courses/PPT.
3. Pak passende fragmenten uit de juiste quote-bank (`quote-bank-blog`, `-nerdio`, `-salomon`, `-twitter`, `-replies`) als ruw stemmateriaal, niet om te kopiëren maar om de cadans te raken.

## Stap 4: De pack samenstellen
Lever de bundel in dit vaste format:

```
WRITING-PACK: <onderwerp>
Kanaal / register / taal: <...>
De route (reframe): <de niet-voor-de-hand-liggende insteek; welke premisse je eerst rechtzet>
Posities (3-6):
  - <stance in 1 zin>  [bron: <bestand.md>]
  ...
Feiten (met bron + verificatiestatus):
  - <feit>  [bron: <bestand.md> | live geverifieerd: <ja/nee/n.v.t.>]
  ...
Voice-guardrails:
  - register: <BvK vol / Nerdio corporate-warmed>
  - open: <LinkedIn enthousiasme-hook / relocate-the-question>
  - close: <hand-off + CTA om toe te passen>
  - banned-word scan: draaien voor tonen
  - geen em-dashes; geen AI-staccato; geen performed warmth
Open vragen / gaten: <ontbrekende positie of te verifiëren feit>
```

## Stap 5: Draften (als Bas een draft wil)
1. Schrijf vanuit de pack, in het gekozen register. Bouw op de route: weiger de voor-de-hand-liggende opening, zet de premisse recht, loop een picture-able pad.
2. Waarde-voor-de-lezer is de eindtoets: leert het iets, maakt het iemands werk makkelijker?
3. Draai de banned-word scan uit het voice-profile. Geen em-dashes. Geen korte punch-zinnen als ritme-trucje (zie voice-corrections).
4. Toon de draft. Houd 'm aan de korte kant voor LinkedIn (Bas gebruikt vaak niet de volle lengte).

## Stap 6: Leren
Keurt Bas een woord of wending af, log het direct in `standaarden/voice/voice-corrections.md` (afgekeurd, beter, waarom, datum). Herhaalt een patroon zich, promoveer het naar de NEVER-lijst in `voice-profile.md`.

## Harde regels (altijd)
- Never invent; verifieer feiten, flag bij twijfel.
- Geen em-dashes, nergens.
- Juiste voice per kanaal, banned-word scan voor alles dat zijn stem draagt.
- Nooit privecontext uit het voice-profile in output.
- NMB/FIRE/financien horen niet in dit brein en gaan alleen via het Academy-kanaal (Nederlands).

## Verwante notities
- [Positie-digest: signature stances (schrijf-kompas)](../../kennis/positie-digest.md)
- [Brein-index (master)](../../kennis/index.md)
