# CLAUDE.md — Exocortex

Dit is mijn second brain: een persoonlijke kennisbasis in markdown, door mij beheerd, door jou doorzoekbaar en bewerkbaar. Behandel de bestanden hier als de bron van waarheid. Herhaal hun inhoud niet, verwijs ernaar.

Ik communiceer in het Nederlands. Deliverables zijn meestal Engels (zie de output-taalregel hieronder).

## Mappen
- `kennis/` — mijn vakinhoud, gedistilleerd. Niet de volledige tekst, de essentie.
- `beslissingen/` — keuzes met datum en waarom, zodat ze navolgbaar zijn.
- `standaarden/` — mijn vaste regels en systemen. Index: `standaarden/README.md`.
- `inbox/` — ruwe dump, nog niet geordend. Twijfel over plek? Hier.
- `archief/` — achterhaald maar bewaard.

## Altijd, bij elke vraag
- Zoek eerst in `kennis/`, `beslissingen/` en `standaarden/` voordat je uit algemene kennis antwoordt.
- Filter eerst op frontmatter (`type`, `merk`, `domein`, `status`, `datum`), dan pas op inhoud. De conventie staat in `README.md`.

## Brein-onderhoud (altijd)
Het brein is een web, geen stapel. Volg `standaarden/brein-onderhoud.md`:
- Leg verbanden: elke notitie die je maakt of aanraakt krijgt links naar verwante notities, twee kanten op.
- Werk ongevraagd bij: bij nieuwe input (gesprek, memo, transcript, artikel) update je geraakte notities, verzoen je tegenstrijdigheden en signaleer je gaten. Wacht niet tot ik vraag om te archiveren.
- Leg ook posities vast (`type: positie`), niet alleen feiten.

## Standaarden (lees voor je iets maakt dat mijn stem of stijl draagt)
- Voice: `standaarden/voice/voice-profile.md` — de stem en de register-dial (BvK vs Nerdio).
- Afgekeurde wendingen: `standaarden/voice/voice-corrections.md` — concrete woorden en zinnen die niet van mij zijn. Lees mee met het profiel en vul aan als ik iets afkeur.
- Schrijfregels: `standaarden/schrijfregels/` — content-guard, het volledige Nerdio-stijlboek, en de output-taalregel.
- Visueel: `standaarden/visuele-systemen/` — BvK editorial skin en Nerdio-skin.
- Workflows: `standaarden/workflows/` — productie-recepten (bijvoorbeeld pdf-naar-podcast).

## Voor je iets in mijn stem schrijft
1. Lees `voice/voice-profile.md` en `voice/voice-corrections.md`.
2. Kies de juiste voice per kanaal (register-dial): volle BvK-stem voor LinkedIn, blog, carousels en alles wat ik over Nerdio publiceer. Nerdio corporate-warmed voor officiele Docebo-lessen, courses en formele PPT.
3. Output standaard in het Engels. Nederlandse uitzondering: het Academy/finance-kanaal. De regel met details staat in `standaarden/schrijfregels/output-taal-engels.md`.
4. Draai de banned-word scan uit het voice-profile voordat je iets toont.

## Voor Nerdio-content
Volg `standaarden/schrijfregels/nerdio-content-guard.md`: American English, Nerdio-terminologie, en de never-invent regel. Verifieer elke technische claim live tegen de officiele bron (NME Help, NMM Help, Microsoft Learn). Niets uit geheugen. Bij twijfel flag je het, je gokt niet.

## Harde regels
- Geen em-dashes in output: alles wat je uit het brein haalt, samenstelt, beantwoordt of nieuw schrijft. Bestaande brein-inhoud mag ze bevatten en hoeft niet opgeschoond. Neem je tekst of een citaat uit het brein over, vervang de em-dash dan (komma, dubbele punt, haakjes of een nieuwe zin).
- Verifieer feiten voordat je ze stelt. Never invent. Bij twijfel flaggen, niet gokken.
- Nooit privecontext uit het voice-profile (het blok onderaan dat bestand) in output. Dat is alleen voor calibratie.
- Pas de juiste voice toe per kanaal, en run de banned-word scan voor alles dat mijn stem draagt.

## Werkwijze (volledig in `werkwijze.md`)
Dit brein is de bron van waarheid. Waardevolle output schrijf je weg naar de juiste map. Committen en pushen doe je pas als ik "commit" zeg (zie "Pas pushen op mijn teken"). Alleen wat gepusht is, staat veilig.

## Notes on the go
Notities die ik vanaf mijn telefoon inspreek. Uitleg voor de map zelf: `inbox/README.md`.
- Begint een sessie: eerst `git pull`, zodat je op de laatste stand werkt.
- Begint een bericht met "Notitie:" of "Note:", sla het op als nieuw bestand in `inbox/` met de naam `JJJJ-MM-DD-korte-titel.md` (titel in het Engels, kleine letters, koppeltekens).
- Notities komen via spraak binnen, in het Nederlands of Engels. Sla ze altijd op in het Engels. Vertaal Nederlands naar natuurlijk Engels, maar laat eigennamen en Nederlandse projectnamen (zoals Nooit Meer Blut, Altijd in Bèta) onvertaald.
- Schoon de dicteertekst licht op: interpunctie, spelling, vaktermen goed geschreven (Nerdio, AVD, Windows 365, Intune, Docebo). Verander de inhoud niet, voeg niets toe, vat niet samen.
- Bovenaan frontmatter met de datum en de regel `source: phone`, plus de verplichte velden uit `README.md` (`type: idee`, `status: concept`, `merk` en `domein` naar beste inschatting).
- Sla op in `inbox/`, maar commit en push pas als ik "commit" zeg. Dan naar main, geen aparte branch.

## Kort-modus
Eindigt een vraag of opdracht op het woord "kort" (getypt of ingesproken), dan antwoord je beknopt.
- Denk eerst goed na, vat daarna sterk samen. Alleen de kernpunten, geen grote lap tekst.
- Geldt voor alles: antwoorden uit het brein, opzoekwerk op internet, uitleg en statusmeldingen.
- Waarschuwingen, twijfels en niet-geverifieerde claims noem je ook in kort-modus, in een regel.
- Zonder "kort" antwoord je zoals gewoonlijk.

## Snooker-notities
Snooker heeft een eigen sectie: `domein: snooker`, met `kennis/index-snooker.md` als knooppunt.
- Is een notitie ("Notitie:" of "Note:") over snooker, of zeg ik dat erbij, dan gaat hij niet naar `inbox/` maar direct naar `kennis/`, met dezelfde naam- en taalregels als hierboven.
- Frontmatter: `domein: snooker`, `merk: bvk`, `type: idee`, `status: concept`, `source: phone`, plus `tags: [snooker]`.
- Zet de notitie bovenaan onder "Notities" in `kennis/index-snooker.md` en link vanuit de notitie terug naar de index. Leg ook links naar verwante snooker-notities.
- Twijfel of het over snooker gaat: vraag het, of zet hem in `inbox/`.
- Pushen pas als ik "commit" zeg, net als bij andere notities.
- Snooker-nieuwsbrief: vraag ik naar de snooker-nieuwsbrief, de snooker-serie, snooker en mijn carriere, of iets in die richting, start dan bij `kennis/snooker/newsletter/README.md` (serieplan, beslissingen, open vragen, drafts per editie). Nieuwe edities komen in die map als `NN-korte-titel.md`. De serie loopt binnen EUC News Nuggets, zonder namen van personen.
- Trainingsverslagen (een snooker-training die ik doorgeef) gaan naar `kennis/snooker/training/`, een bestand per sessie, volgens de conventie en het template in `kennis/snooker/training/README.md`. Zet de sessie bovenaan onder "Sessions" in die README.

## Projectmappen
Lopend werk met een eigen map onder `kennis/<project>/`, met `README.md` als startpunt. Alleen publieke informatie, geen Nerdio-IP (zie `beslissingen/projectmappen-nerdio-werk.md`).
- Citrix Reskilling: vraag ik naar de Citrix Reskill course, Reskilling of de Reskill Edition, start dan bij `kennis/citrix-reskilling/README.md`.

## Opruimen (elke sessie)
Ik wil geen losse eindjes. Het einde van een sessie is niet te detecteren, dus de controle draait op twee momenten: bij de start van elke sessie (direct na `git pull`) en na elke afgeronde taak.
- Controleer: staan er lokale wijzigingen die nog niet gecommit of gepusht zijn? Staan er branches op GitHub naast `main` (`git ls-remote --heads origin`)?
- Ruim zelf op wat zeker klaar is: branches verwijderen die volledig in `main` zitten. Niet-gepusht werk push je niet zelf, dat meld je (zie hieronder).
- Twijfel (een branch met werk dat niet in `main` zit, een bestand waarvan je niet weet of het weg mag): niets verwijderen, mij eerst kort vragen.
- Meld in een regel wat je gecontroleerd en opgeruimd hebt. Was alles schoon, zeg dat dan ook kort.

## Pas pushen op mijn teken
In cloud-sessies commit en push je niets uit jezelf. Je schrijft wel weg naar de juiste map, maar het gaat pas naar GitHub als ik "commit" zeg.
- Na elke taak meld je in een regel wat er klaarstaat en nog niet gepusht is, zodat ik weet dat ik "commit" moet zeggen.
- Niet-gepusht werk verdwijnt als de werkplek wordt opgeruimd. Waarschuw daarom duidelijk als er iets klaarstaat.
- Zeg ik "commit": commit en push alles wat klaarstaat naar main.

## Processing the inbox
Zeg ik "verwerk de inbox" of "process the inbox":
1. Lees elke notitie in `inbox/` (behalve `README.md`).
2. Stel per notitie voor waar hij hoort: een nieuw bestand (welke map, welke naam) of een toevoeging aan een bestaand bestand (welk, en waar). Noem ook de links die je wilt leggen.
3. Hoort iets bij NMB of FIRE, dan zeg je dat het buiten dit brein valt in plaats van het te archiveren.
4. Wacht op mijn akkoord. Pas daarna verplaatsen of samenvoegen, frontmatter bijwerken, verbanden leggen volgens `standaarden/brein-onderhoud.md`, en committen en pushen.

## Niet hier
- Nooit Meer Blut (NMB) hoort niet in dit brein. Apart project, buiten deze repo beheerd. FIRE valt onder NMB en staat hier dus ook niet. Beide zijn wel volle BvK-stem en Nederlands.
