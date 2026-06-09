PDF → Artlist Podcast Script Workflow

A repeatable step-by-step recipe for turning a Nerdio Microlearning PDF into a TTS-ready script for Artlist, recorded in Finn's voice. Distilled from the Compass build in May 2026.



Why this exists

The PDFs are designed for the eye: page numbers, step headers, stat boxes, checkmarks, em dashes, arrows. None of that survives a text-to-speech engine cleanly. A direct paste makes Finn sound like a robot reading a slide deck. This guide makes him sound like Finn reading a lesson.

The principle: preserve every fact, figure, claim and structural beat from the PDF. Rewrite the form, not the content.



Hard constraints (Artlist, May 2026)



5000 characters per TTS generation — anything longer needs to be split.

A full microlearning is typically \~1.000–1.300 words ≈ 6.000–7.500 characters when rewritten — so almost always two parts.

Spoken pace at default settings is \~150 wpm. A 1.100-word script = \~7 minutes.

Plain text only. No markdown, no formatting. .txt files are easiest to paste.





The workflow at a glance



Extract clean text from the PDF

Strip visual scaffolding

Convert visual elements to flowing prose

Spell out symbols, numbers and UI paths

Add narrative transitions

Write a proper intro and outro

Split into two parts at a natural cliffhanger

Save as two .txt files

Record both halves in Artlist (Finn voice)

Splice in an audio editor

Upload MP3 to Audio/ folder on GitHub





Step 1 — Extract clean text from the PDF

Use pdftotext on the source PDF. This gives raw text without layout junk, but with page numbers and footers still in. Word-count check confirms you have the whole thing — a Compass-sized lesson is \~1.000–1.200 words from pdftotext.

bashpdftotext source.pdf - | wc -w

pdftotext source.pdf draft.txt

You now have a draft. Do not edit the PDF. Only the script.



Step 2 — Strip visual scaffolding

These elements come from pdftotext and add nothing to the audio. Remove every instance:

Scaffolding elementExampleActionPage numbers01 / 08, 02 / 08DeletePage footersNERDIO MICROLEARNING · COMPASSDeleteCover-page bitsEDITION 2026, MICROLEARNING, the standalone author bylineDelete (becomes intro instead — see Step 6)Step headersSTEP 1 · WHY THIS LESSONDelete and replace with narrative transitionNumbered markers as headers01, 02, 03 standing alone above paragraphsDelete or fold into proseBold ALL-CAPS sub-headersWITH COMPASS, TODAY, TAKE-AWAYDelete or rephrase as a spoken cue (see Step 5)Pull-quote markers", " (the curly quotes that wrap insight quotes)Delete the quote marks; keep the words; preface naturally

Why: a TTS engine reads "STEP 1 dot WHY THIS LESSON" out loud. It also reads "01" as "zero one" or "oh-one". Both are jarring. Strip them.



Step 3 — Convert visual elements to flowing prose

The PDF design uses visual layout to do work that, in audio, has to be done by sentence structure. Convert each visual pattern below into prose that carries the same information.

3a. Stat blocks

PDF visual:

1,400      3        8mo               40%

USERS      SITES    UNTIL RENEWAL    ESTIMATE SPREAD

Spoken rewrite (one sentence, all four facts intact):



So: fourteen hundred users, three sites, eight months until renewal, and a forty percent spread between estimates. That is the starting point.



3b. Checkmark lists with three columns

PDF visual:

✓ Read-only       ✓ Tier scoring          ✓ Five destinations

\[short line]      \[short line]            \[short line]

Spoken rewrite (as a "three things" callout):



Three things make this work. \[Read-only explanation]. \[Tier scoring explanation]. And \[five destinations explanation].



3c. Four-pillar grids

PDF visual: 2x2 grid of named pillars with sub-bullets each.

Spoken rewrite: introduce as "X works across four dimensions", then take each pillar as a paragraph: "The first dimension is...", "The second dimension is...", etc. Bullets inside each pillar become flowing sentences.

3d. Code paths and UI breadcrumbs

PDF visual: Endpoints > Policy Management or Settings > Environment > Intune

Spoken rewrite: Go to Endpoints, then Policy Management. or Open Settings, then Environment, then Intune.

The > symbol is unreadable for TTS. Spell out the navigation.

3e. Tables

Read row-by-row as sentences. Keep the order. If a table has 3+ columns, restructure as "X has \[col2], \[col3], and \[col4]" per row.

3f. Pull-quote insight pages

PDF visual: huge quote in italics with quote marks, often the climax of the lesson.

Spoken rewrite: preface and keep the words intact.



And here is the insight to remember. \[the quote, no quote marks].





Step 4 — Spell out symbols, numbers and dates

TTS engines pronounce these inconsistently. Always spell them out.

Symbol replacements

SymbolReplace with%"percent" — 40% → "forty percent"€"euros" — €58k → "fifty-eight thousand euros"$"dollars" — USD 0.40 → "forty cents" or "zero point four zero dollars"→spell the relationship — "leads to", "becomes", "moves to"↗ ↓delete (these are UI hints, not spoken)·comma or full stop, whichever fits the rhythm— (em dash)comma, or split the sentence with a full stop\&"and"+"plus"\~"roughly" or "around"

Number pronunciations

WrittenSpoken1,400"fourteen hundred" (cleaner than "one thousand four hundred")100-point"hundred-point"80 and above"eighty and above"6 to 12 month"six to twelve month"90 min"ninety minutes"Q1, Q2"the first quarter", "the second quarter"v8.0"version eight point zero"2026"twenty-twenty-six" (more natural than "two thousand twenty-six")

Date pronunciations

WrittenSpokenMay 5, 2026"May fifth, twenty-twenty-six"May 4, 2026"May fourth, twenty-twenty-six"2026-05-05always rewrite to month-day-year prose

Product names — leave intact

Azure Virtual Desktop, Windows 365, Nerdio Manager for Enterprise, Microsoft Entra ID, Intune, Citrix DaaS — all spoken naturally by Artlist. Don't substitute or abbreviate.

Acronyms — case-by-case



AVD → leave as "AVD", spoken letter-by-letter ("ay vee dee")

VDI → leave as "VDI"

HCI → leave as "HCI"

CIO → leave as "CIO"

CSV → leave as "CSV"

RBAC → spell out: "role-based access control"

UPN → spell out on first use: "user principal name"

CA (Conditional Access) → spell out on first use, then "CA" is fine





Step 5 — Add narrative transitions

A spoken lesson needs connective tissue that the PDF doesn't, because the PDF uses headers and visual breaks to do that work.

Replacement patterns

PDF patternSpoken bridgeSTEP 1 · WHY THIS LESSON"Three things to keep in mind before we start."STEP 2 · WHAT IT IS"So what is \[product]." or "Here's what it actually is."STEP 3 · FOUR PILLARS"\[Product] works across four dimensions."STEP 4 · HOW IT WORKS"From \[start state] to \[end state], in \[N] moves."STEP 5 · THE INSIGHT"And here is the insight to remember."STEP 6 · IN PRACTICE"Here is how this plays out."STEP 7 · NOW YOU TRY"Before we close, \[N] questions to chew on."TAKEAWAY (final block)"The takeaway. \[the takeaway line]."01, 02, 03 as ordered numbering"First...", "Second...", "Third..."

Internal transitions

Inside a paragraph, when the PDF has a hard visual break but the script should flow:



"Then \[next thing]."

"On top of that, \[next thing]."

"So far so good. The next move is..."





Step 5b — Make Finn sound human (Eleven V3 layer)

Artlist runs on ElevenLabs V3 under the hood. V3 has three inline mechanisms that turn a clean, well-structured script into something that sounds like a person reading, not a TTS engine reading. Layer them — but sparingly. Overuse breaks the spell faster than underuse.

5b.1 — Discourse markers (biggest "human" lever, smallest effort)

Short opening words humans use to think out loud. Sprinkle them on 3 to 5 sentences per part — no more. Beyond that the narrator stops sounding confident and starts sounding hesitant.

Use: OK, So, Now, Look, Right, Well.

Don't use: "you know", "I mean", "actually", "basically" — these are precisely the fillers Bas avoids in writing. They don't get a pass in audio either.

Always comma after the marker. OK, here is the takeaway. not OK here is the takeaway. Without the comma, V3 swallows the marker and you lose the beat that makes it sound human.

Good spots:



Transition into a new section: "OK, three things to keep in mind before we start."

Pivot in the scenario: "Now, with Policy Studio."

Lead-in to the insight: "Look, here is the insight to remember."

Lead-in to the takeaway: "Right, the takeaway."



5b.2 — Topic labels: use lead-in sentences, not single-word labels

Single-word topic labels followed by a colon are forbidden in the script. The pattern to avoid: \[single word or short phrase]: followed by explanation. A TTS engine treats the label as a standalone sentence — the voice drops on the word, makes a mental stop, and then restarts with the explanation. Stress and intonation do not connect.

The topic must always be embedded in a full sentence that grammatically flows into the explanation:

Do not useUse instead\[single word or short phrase]: followed by explanationA full sentence that introduces the topic and flows into the explanationLaunch: announced at NerdioCon...When it comes to the launch, it was announced at NerdioCon...Foundation: built on the existing Intune integration...As for what it is built on, it runs on the existing Intune integration...Coexistence: the native Intune admin center keeps working.And it works alongside what you already have — the native Intune admin center keeps working.

Exception: ordered lead-in words like "First,", "Second,", "Third," are fine — they are grammatically an approach and let the voice flow directly into the explanation that follows.

5b.3 — Audio tags (V3's emotion controls)

Inline tags in square brackets steer V3's emotional read of the next sentence. Bigger lever for human-sounding output than the stability slider.

TagUse for\[warm]intro greeting, outro sign-off, friendly transitions\[matter-of-fact]facts, stats, definitions — the "what it is" beats\[confident]the takeaway line, the final block\[deadpan]a punchline that should land flat ("zero native undo")\[casual]the questions section, the practice prompt\[chuckles softly]a light beat — use once per script, max\[thoughtful pause]before a complex insight\[friendly]scenario openers ("So, today.")

Place the tag on its own at the start of a sentence or paragraph. It colours everything after it until the next tag or paragraph break.

5b.4 — Pause tags and ellipses (timing)

V3 supports three explicit pause tags that no other model has:



\[short pause]

\[pause]

\[long pause]



Use these for hard timing moments where the silence is doing the work — a comedic beat, the cliffhanger before "insight to remember", the breath before the takeaway. Example: And I should say up front \[pause] this is the part most teams skip.

For softer breath-pauses inside a sentence, use ellipses (...). V3 reads them as real breathing beats. Example: First, in Intune you can push a policy... you cannot pull it back.

Note: SSML <break time="1.5s"/> tags do NOT work in V3 — they work in every other ElevenLabs model, but V3 ignores them. Use bracket tags or ellipses instead.

5b.5 — Don't stack tag + marker on the same sentence

If a sentence already has an audio tag like \[casual] or \[matter-of-fact], don't also start it with a discourse marker. Pick one. Stacked, V3 reads both and the tone gets overcooked — the narrator sounds like he's trying too hard.

5b.6 — Artlist generation settings



Stability: 0.4 — not the default 0.5. Below 0.35 starts producing hasty, glitchy reads.

Effect: No Effect — don't apply Artlist's built-in colouring effects on top of the audio tags. They fight each other.

Generate 2 to 3 times. V3 is non-deterministic. Even with identical input, the read varies. Pick the best take per part.





Step 6 — Write a proper intro and outro

The cover page and the back page don't translate. Replace with a recurring intro/outro template — this also makes the podcast feel like a series.

Important — framing rule: Finn narrates OVER Bas's content, not AS Bas. The intro/outro must refer to Bas in the third person ("by Bas van Kaam", "from Bas van Kaam's book"). Never have Finn say "I'm Bas van Kaam" or "my book" — it creates the audience-confusing impression that Finn IS Bas.

Intro template — Nerdio Microlearning (\~50 words)



This is a Nerdio Microlearning by Bas van Kaam, Principal Training Architect at Nerdio. Edition twenty-twenty-six. Today: \[LESSON TITLE] — \[SUBTITLE]. About \[N] minutes. No fluff.



(Substitute \[LESSON TITLE] and \[SUBTITLE] from the PDF cover. N = readMin from the entries array.)

Intro template — book chapter (\~50 words)



This episode is a chapter from Bas van Kaam's book on \[TOPIC]. Today: \[LESSON TITLE] — \[SUBTITLE]. About \[N] minutes. No fluff.



Outro template — Nerdio Microlearning (\~40 words)



\[The takeaway line, often three short sentences from the back page.]

That was a Nerdio Microlearning by Bas van Kaam, Principal Training Architect at Nerdio. If this was useful, share it with one colleague \[contextual hook from the lesson, e.g. "currently planning a VDI modernization"].

Until next time.



Outro template — book chapter (\~40 words)



\[The takeaway line, often three short sentences from the source.]

That was a chapter from Bas van Kaam's book on \[TOPIC]. If this was useful, share it with one colleague \[contextual hook]. Until next time.





Step 7 — Split into two parts

Almost every lesson exceeds 5.000 characters after rewriting. Split at a natural narrative break, not at a character count.

How to find the split point



The "insight to remember" climax is almost always the right place. It's the highest emotional/intellectual beat of the lesson. Ending part 1 there leaves the listener with the takeaway already lodged.

Part 2 then opens directly with the next narrative beat — for example Here is how this plays out, or a fresh audio tag plus the next content line. No "welcome back" bridge — see "Part 2 opener" below.



Target sizes



Part 1: 4.000–4.900 characters. Aim for headroom under the 5.000 cap.

Part 2: 2.000–3.500 characters. Almost always shorter, because the back half of a lesson (scenario, questions, outro) is denser per character.



Sanity check

After splitting, check character counts:

bashwc -c part1.txt part2.txt

If part 1 is over 4.900, look for an earlier natural beat (end of the four-pillar section, or end of "what it is") and move some content into part 2.

Part 2 opener — default: seamless transition

By default Bas mixes part 1 and part 2 into a single continuous episode, so part 2 must NOT open with a "welcome back" bridge. Pick up directly after the part 1 cliffhanger with the next narrative beat:



"Here is how this plays out."

"Now, here is where it gets interesting."

Just a fresh audio tag like \[deadpan] or \[matter-of-fact] plus the next content line.



Only use a bridge opener like "Welcome back" if Bas explicitly says the parts will stay separate (different episodes, paused playback, etc.).



Step 8 — Save as plain text files

Filename convention:

<topic>\_part1.txt

<topic>\_part2.txt

Examples:



compass\_part1.txt + compass\_part2.txt

intune\_policy\_studio\_part1.txt + intune\_policy\_studio\_part2.txt

avd\_hybrid\_part1.txt + avd\_hybrid\_part2.txt



No markdown. No section headers in the text itself. Section markers (like ## Intro) belong only in your own drafting copy, never in the file you paste into Artlist — TTS reads "hashtag hashtag intro" out loud.

Paragraph breaks (double newlines) are fine. Artlist treats them as natural pauses.



Step 9 — Record in Artlist



Open Artlist AI Voice Generator.

Select Finn's voice (or the chosen narrator profile — keep it the same across all lessons for series consistency).

Paste part1.txt content into the prompt box.

Generate. Listen back.

If a sentence sounds off (wrong stress, weird pronunciation, awkward pause), tweak that sentence in the script and regenerate. Common fixes:



Add a comma to slow down

Spell out a number that sounded off

Break a long sentence into two





Download the MP3 of part 1.

Repeat steps 3–6 for part2.txt.





Step 10 — Splice the two halves

In any audio editor (Audacity, GarageBand, Reaper, even Premiere):



Drop part 1 MP3 on the timeline.

Drop part 2 MP3 immediately after, with a 0.6–0.9 second gap between them. That gap masks the splice and feels like a natural breath.

Trim any leading or trailing silence.

Export as a single MP3, 96 kbps mono is plenty for spoken word and keeps file size around 5 MB for a 7-minute episode.





Step 11 — Upload to the site

Filename convention matches the PDF:

PDFs/Nerdio\_Compass\_MicroLesson\_LinkedIn.pdf

Audio/Nerdio\_Compass\_MicroLesson\_LinkedIn.mp3

Same base name, different folder, different extension. The entries array in index.html then gets an audio field on that entry:

jsaudio: 'Audio/Nerdio\_Compass\_MicroLesson\_LinkedIn.mp3'

The Listen button appears automatically once the field is set. The card renders the 3-button outlined-pill layout (Read + Listen + Download).



What stays unchanged from the PDF (the no-fly zones)



All facts, figures, dates, dollar/euro amounts, percentages. If the PDF says forty percent, the script says forty percent. No rounding, no rephrasing of the number itself.

Product names, exact and case-correct: "Azure Virtual Desktop" not "AVD" on first mention; "Microsoft Entra ID" not "Entra".

The structural beats: why → what → how → insight → practice → questions → takeaway. The lesson's spine is the lesson's spine.

Bas's voice: anti-fluff, practical, lessons "earn their time", quietly opinionated about the field. The script must read like Bas wrote it, even though Finn reads it.





Things to avoid



Don't change facts to make a sentence flow better. Restructure the sentence instead.

Don't drop the practical scenario — that's the part listeners remember.

Don't insert phrases Bas wouldn't say. No "Hey folks", no "let's dive in", no "buckle up". The bar is: would this make Bas wince?

Don't use em dashes in the script. TTS sometimes reads them as the word "dash". Always replace with a comma or a full stop.

Don't keep STEP headers in the file — even commented out, even prefixed with #. Artlist may read them.

Don't paste markdown formatting into Artlist. Asterisks, backticks, brackets — all read out loud.

Don't use "you know", "I mean", "actually", "basically" as discourse markers. They are the verbal version of corporate filler. Stick to OK, So, Now, Look, Right, Well.

Don't repeat the title in part 2's opener. Part 2 picks up right where part 1 ended; saying "welcome back to the Nerdio Compass microlearning" is jarring on a continuous listen.





Reference: the Compass build (May 2026)

MetricValueSource PDFNerdio\_Compass\_MicroLesson\_LinkedIn.pdfSource pages8Source word count (pdftotext)1.047Script word count\~1.100Script total characters\~7.036Part 1 characters4.724Part 2 characters2.312Split pointAfter "insight to remember" climaxSpoken duration estimate\~7 minutes totalAudio pathAudio/Nerdio\_Compass\_MicroLesson\_LinkedIn.mp3



Quick checklist before you paste into Artlist



&#x20;All page numbers removed

&#x20;All STEP headers removed

&#x20;All stat blocks rewritten as prose

&#x20;All > paths replaced with "then" sequences

&#x20;All %, €, $, \&, +, \~ spelled out

&#x20;All em dashes replaced with commas or full stops

&#x20;All dates pronounced as "month-day, year"

&#x20;All "01, 02, 03" numbering replaced with "First, Second, Third"

&#x20;Intro template applied (with current title and minutes)

&#x20;Outro template applied (with current lesson hook)

&#x20;Part 1 under 5.000 characters

&#x20;Part 2 under 5.000 characters

&#x20;Part 2 transitions seamlessly (no "welcome back" bridge unless parts stay separate)

&#x20;No markdown, no headers, no asterisks in either file

&#x20;3 to 5 discourse markers per part, comma after each

&#x20;Audio tags placed on the right beats (warm intro, confident takeaway)

&#x20;Pause tags or ellipses on the cliffhanger and insight

&#x20;No tag + marker stacked on the same sentence

&#x20;Stability 0.4, Effect: No Effect, 2-3 generations per part

