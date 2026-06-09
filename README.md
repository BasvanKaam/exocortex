# Second Brain

Mijn persoonlijke kennisbasis. Platte markdown, door mij beheerd, door Claude doorzoekbaar.

## Mappen

- `kennis/` - Wat ik weet. Gedistilleerde vakinhoud, kernpunten uit boeken, artikelen, cursussen. Geen volledige teksten, alleen de essentie.
- `beslissingen/` - Wat ik koos en waarom. Architectuurkeuzes, strategie, met datum. Zodat een keuze later navolgbaar is.
- `standaarden/` - Mijn vaste regels. Naming, schrijfstijl, visual styles, voice. Dit bewaakt consistentie over alles wat ik maak.
- `inbox/` - Ruwe dump. Hier gaat alles in wat nog geen plek heeft. Wordt periodiek opgeschoond en verplaatst.
- `archief/` - Achterhaald maar bewaard. Niets weggooien, alleen uit de weg.

## Regel: niet overdenken

Twijfel je waar iets hoort? In `inbox/`. De wekelijkse opschoonrun verplaatst het wel.

## Tag-conventie

Elke notitie begint met frontmatter (zie `_template.md`). Vijf velden zijn verplicht:

- `type` - kennis | beslissing | standaard | bron | idee
- `merk` - bvk | nerdio. De merk-as: van wie is dit. Standaard `bvk` (mijn eigen werk), `nerdio` alleen voor officieel Nerdio-werk.
- `domein` - nerdio | nmb | podcast | euc | persoonlijk | financieel | ai-tooling. Het onderwerp, los van het merk.
- `status` - actief | concept | achterhaald
- `datum` - aanmaakdatum, formaat JJJJ-MM-DD

`tags` is vrij en optioneel: losse trefwoorden voor fijnzoeken.

Waarom dit telt: de zoeklaag filtert eerst op deze velden voordat hij de inhoud doorzoekt. Goede frontmatter betekent dat een vraag over Nerdio niet je financiele notities meesleept.

## Conventies

- Geen em-dashes, nergens.
- Bestandsnamen in kleine letters met koppeltekens: `windows-365-flex.md`.
- Eén onderwerp per notitie. Liever tien korte dan een lange.
