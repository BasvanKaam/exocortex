name: nerdio-content-guard

description: Enforce Nerdio L\&D writing style and live-verify every technical claim before any text is committed to a deliverable. Apply whenever writing, generating, or composing text that will appear in Nerdio content — microlearnings, carousels, lessons, course descriptions, video scripts, learner journey copy, ADDIE documents, social posts, blog text, or any other artifact. Triggered automatically by nerdio-microlesson and nerdio-content skills before they generate any text. Triggered standalone when the user says "check this writing", "rewrite in Nerdio style", "write the Nerdio way", "make sure this is American English", "verify the technical claims in this draft", or any phrase implying style enforcement or factual checks. Always uses American English (never European/British). Always verifies technical claims live against Nerdio help docs, Microsoft Learn, and the Microsoft Writing Style Guide before output.

Nerdio Content Guard: writing rules + live verification

This skill is the writing/content layer that sits on top of all Nerdio L\&D output. It does NOT govern visual design, layout, fonts, colors, or page geometry — those belong to the parent skill (e.g. nerdio-microlesson). This skill governs how text is written and whether what is written is true.

Two responsibilities:



Style enforcement. Every word and sentence follows the Nerdio L\&D Style Guide (nerdio\_style\_guide\_reference\_v3\_md.txt). American English, not European/British.

Live technical verification. No technical claim leaves this skill without being verified against an authoritative source (Nerdio help docs, Microsoft Learn, vendor docs). Nothing is invented. Nothing is from memory if it's even slightly uncertain.



What this skill does NOT do: set the register. The voice/tone level is chosen per deliverable from VOICE\_PROFILE\_Bas\_van\_Kaam\_FINAL.md, not here: BvK full voice for carousels, LinkedIn, and anything written about Nerdio; Nerdio corporate-warmed for official Docebo lessons, courses, and formal PPT. The split stays clean: this skill governs WHAT you say (words, claims, terminology, American English, verified facts), the voice profile governs HOW you explain (rhythm, warmth, texture) inside those constraints. Load the profile alongside this skill before writing, and run its mandatory banned-word scan before output.



When to use this skill

Trigger automatically:



When nerdio-microlesson is generating slide text

When nerdio-content is producing lessons, ADDIE docs, video scripts, course descriptions, learner journey copy

Before any text is written into a deliverable that will be shipped to Bas



Trigger standalone:



"Check this writing for Nerdio style"

"Rewrite this paragraph the Nerdio way"

"Make sure this is American English"

"Verify the technical claims in this draft"

"Apply the style guide to X"

"Check this against the Nerdio writing rules"



Do NOT use this skill for:



Visual design, layout, typography decisions (those live in the parent skill)

Reviewing already-finished documents with tracked changes (use nerdio-review)

Content that is explicitly NOT Nerdio L\&D (Bas's personal blog, BTW returns, etc.)





Mandatory pre-writing workflow

Run this workflow before producing the first sentence of any deliverable. It cannot be skipped.

Step 1: Identify everything that needs verification

Read the topic brief. List every:



Product name (Nerdio Manager for Enterprise, Azure Virtual Desktop, Microsoft Intune, Windows 365, etc.)

Feature name (Policy Studio, Auto-scale, App Attach, Cloud PC, FSLogix profile container, etc.)

Technical term (UPN, RBAC, Conditional Access, Microsoft Graph, etc.)

Procedure / UI path (e.g. Settings > Environment > Intune)

Role / permission name (e.g. Read Approvals, Manage Approvals)

Pricing figure, license requirement, version number, GA / preview status, launch date

Any acronym, abbreviation, or capitalization choice you are not 100% certain about

Any single technical word where the spelling/capitalization could go either way (sign in, on-premises, App Attach, Cloud PC, etc.)



If the list is empty the lesson has no technical content — proceed to style. If it has any items at all, do Step 2.

Step 2: Live-verify every item from Step 1

For each item, search authoritative sources before committing it to the deliverable. Use web\_search for finding the source, web\_fetch for reading the full page. Do NOT trust memory.

Authoritative source priority:

Topic areaPrimary sourceURL patternNerdio Manager for EnterpriseNME Helpnmehelp.getnerdio.comNerdio Manager for MSPNMM Helpnmmhelp.getnerdio.comMicrosoft / Azure / Intune / AVD / Windows 365 / Entra IDMicrosoft Learnlearn.microsoft.comMicrosoft writing conventions / word choice / capitalizationMicrosoft Writing Style Guidelearn.microsoft.com/en-us/style-guideOther vendors (Nutanix, etc.)Vendor's official docsvendor's own domainNews / GA dates / launch dates / NerdioCon announcementsVendor announcements + reputable tech newsnerdio.com blog, Microsoft news, etc.

For every technical claim, find at least one authoritative source. Note the URL in your internal reasoning so it can be cited if Bas asks. If you cannot find a source, the claim does not go in. Tell Bas what could not be verified and let him decide.

Important: search results from non-authoritative sources (random blogs, forums, AI-generated summaries on third-party sites) do not count as verification. Only the official sources in the table above qualify.

Step 3: Apply Nerdio style rules

The full reference is nerdio\_style\_guide\_reference\_v3\_md.txt. The non-negotiables are repeated below so they stay in working memory while writing.

Voice and tone



Second person (you), present tense, active voice, imperative for procedures

Encouraging — say what users CAN do, not what they cannot



Wrong: "You cannot upload files larger than 5GB."

Right: "You can upload files up to 5GB."





Help users complete tasks — focus on what they're doing, not on describing features



Wrong: "Nerdio Manager provides automated deployment..."

Right: "Using Nerdio Manager, you can automate the deployment..."





No subjective fillers: easy, simple, simply, just, fast, slow, exciting, difficult

No exclamation points, ever

No jokes, slang, sarcasm, idioms, colloquial language (global audience)

Contractions OK and encouraged for friendly tone (it's, you're, don't, can't, we're) — do not mix contracted and spelled-out in the same sentence; never form a contraction from a noun + verb (no "Nerdio's providing")

Avoid ambiguous contractions (it'll, they'll, there'd, he'd, she'd)

"please" only when asking the user to do something inconvenient caused by the software

"sorry" only in error messages for serious problems

"thank you" only in UI tooltips

Bias-free: they/them/their as singular pronoun; allowlist/blocklist (not whitelist/blacklist); Main branch (not master)

No future tense — use simple present



Wrong: "Nerdio Manager will assign the policies."

Right: "Nerdio Manager assigns the policies."







Punctuation



Oxford / serial comma always: "devices, apps, and policies"

No em dash (—), no en dash (–) — use a simple dash, comma, period, or rewrite. NON-NEGOTIABLE.

No exclamation points, ever

Single space after a period

Comma after introductory adverbial phrases: "On the Settings tab, select + Add."

No ellipsis unless it appears in the UI

Quotation marks: closing punctuation INSIDE for periods and commas, OUTSIDE for other punctuation (American style)

No quotation marks around UI labels, product names, or code — use bold (UI labels), plain text (product names), or Consolas/code font (code)

Semicolons sparingly — prefer two sentences or a list

Colons sparingly — always use a colon to introduce a list; never use a colon to introduce a screenshot

Decades: "the 2000s" — no apostrophe

Apostrophes: noun ending in S takes apostrophe after final S only ("Sales'" not "Sales's")



Numbers



Spell out zero through nine; numerals for 10 and above

ALWAYS use numerals with units: 5GB, 3 CPU, 7 days, 28 days

Don't start a sentence with a numeral — rewrite or spell out

Spell out and hyphenate fractions: "two-thirds" (not 2/3)

% symbol, not the word "percent"

Use commas in numbers with 4+ digits ($1,024; 1,093 MB)

Exception for years and pixels: comma only at 5+ digits (10,000 B.C.)

No commas in page numbers, addresses, or after a decimal point

Don't use ordinal numbers for dates ("June 1", not "June first")



Capitalization



Sentence-style for: document titles, article headings, running text, file/folder/directory names

Title-style for: product names, feature names (Solution Baselines, Scripted Actions), service/tier names (Azure Files Premium, Azure Storage)

UI labels: match the capitalization shown in the UI — except if UI is ALL CAPS, then use title case + bold

Never ALL CAPS for emphasis — use formatting (bold, italic) instead

Don't use internal capitalization unless it's a brand name

Never capitalize the spelled-out form of an acronym unless it's a proper noun

File extensions: all lowercase with a period (.png, .docx)

Department names and titles/roles: capitalize (Technical Solutions department, subscription Owner role)

Company names: check the company website for correct capitalization (e.g. Sophos, Sepago, FSLogix)



Procedures and instructions



Max 7 steps per procedure (Microsoft rule, stricter than Nerdio's 8 — apply 7)

Capitalize the first word of each step

Period at the end of each step (exception: if instructing the user to type input without end punctuation)

If only one step: use a bullet, not a number

Combine simple actions in the same UI location into one step

Always include the action that finalizes a step (OK, Apply, Save buttons)

Use input-neutral verbs — NEVER click (mouse-specific), NEVER tap (touch-specific) unless explicitly describing touch input

select = primary verb for UI interaction. Don't use "highlight" or "pick" as synonyms.

Right angle bracket (>) for simple sequences, max 3 steps: Settings > Integrations. Space before and after, never bold the bracket.

Specify location BEFORE the action in each step

Procedure intro ends with a colon

Introduce a list with a colon

Never introduce a screenshot with a colon



Verbs with UI elements

VerbUse forselectoptions, checkboxes, tabs, links, keys, keyboard shortcuts. NEVER click or tapchooseuser preference / desired outcome onlyclear / unselectremoving a checkbox selection. NEVER uncheck or deselectswitch / turn on / turn offtoggle keys or toggle switchesentertyped or pasted user inputgo to / navigate tomenus, tabs, pages, sidebar panes, bladesopen / close / expandwindows, blades, drop-down menusdisplay (transitive, requires object)use "is displayed" as the passive form. NEVER appear or showdrag / movedragging elements. NEVER "drag and drop" or "click and drag"

Prepositions with UI elements

UI ElementPrepositionWindowinBladeonTabonMenu / drop-down menufrom / inPane / panelinDialog boxinListfrom / in

Terminology — high-risk traps

(See full reference for the complete list. These are the ones most often gotten wrong.)



sign in / sign out — TWO WORDS. NEVER login, log in, log on, signin, logon, log off, logout, log into, log onto, sign into, signoff, sign off, sign on. Exception: if the UI itself uses one of those, match the UI literally.

multifactor authentication (MFA) — never two-factor authentication, never 2FA, no hyphen

on-premises — always hyphenated. NEVER on-prem, NEVER on-premise (premises is plural)

email — no hyphen (not e-mail)

setup (noun) vs set up (verb)

dropdown (noun) vs drop-down (adjective)

back end (noun) vs back-end (adjective). Prefer specific term where possible (server, database, network).

front end (noun) vs front-end (adjective)

failover (noun) vs fail over (verb) vs fail-over (adjective)

Cloud PC — TWO words

App Attach — capitalized as a service name

MSIX app attach — "app attach" lowercase here

FSLogix — exact capitalization

Microsoft Store — both words capitalized

PowerShell, GitHub, WinGet, NetApp, WebSocket — camel case, one word

WiFi — capital W and capital F

OK — never okay or ok

URL, API — all caps

Azure Virtual Desktop (AVD) — spell out on first mention. WVD is deprecated, never use.

Microsoft Intune (Intune) — spell out on first mention

Microsoft Endpoint Manager (MEM) — DEPRECATED, use Unified Endpoint Management (UEM) / Microsoft Intune

internet, online, website, homepage, database, antivirus, nslookup — lowercase, one word

time zone, username — note the spacing/single-word rules

session host or session host VM — never just host

third party (noun) vs third-party (adjective). Always spell out "third" — never "3rd"

add-on, pop-up, opt-in, follow-up, double-click — hyphenated as noun/adjective; two words as verb (add on, opt in, follow up, but double-click always hyphenated)

version numbers: lowercase v, no space (v6.2.1, not "V 6.2.1")

Sysprep — capitalized as the tool name; lowercase as a modifier or verb

re-image — always hyphenated

resize — never hyphenated

Auto-scale / Auto-scaling — hyphen + capital A as the feature name; lowercase as a modifier or verb

single sign-on (SSO) — spell out on first mention, lowercase the spelled-out form

prerequisite — no hyphen

pre-stage — always hyphenated

Zero Trust — both words capitalized



Acronyms — always spell out on first mention in L\&D content



AVD = Azure Virtual Desktop (current — never WVD)

MFA = Multifactor authentication (NEVER 2FA)

UEM = Unified Endpoint Management (replaced MEM)

SSO = Single sign-on

RDP = Remote Desktop Protocol

VDI = Virtual desktop infrastructure

DaaS = Desktop as a service (lowercase, no hyphen, spell out on first mention)

IAM = Identity and access management

MDM = Mobile device management

VPN = Virtual private network

MSP = Managed service provider

MSSP = Managed security services provider



Nerdio brand



"Nerdio" = the company only, never the product

Never make Nerdio plural ("Nerdios")

Never use Nerdio as a verb

Never substitute the logo for the word "Nerdio"

"Nerdio Manager for Enterprise" (full) → "Nerdio Manager" after first mention. NEVER NME in body prose. NME only acceptable in compact contexts (badges, table cells, diagram callouts).

Same rule for "Nerdio Manager for MSP" → "Nerdio Manager", never NMM in body prose

Use "Nerdio Manager" alone only when no confusion with another product is possible

No descriptor words after the product name: never "Nerdio Manager app/platform/portal/console/tool/application"

Plain text only — no bold, no italic, no quotation marks around product names



Microsoft as partner



Always respectful and collaborative

Nerdio adds value ON TOP of Microsoft, never replaces it

Customers must purchase Microsoft first — Nerdio is a layer of value on top

Never frame Microsoft products as problems to be solved

Never headings like "The trouble with Azure"

Spell out the full Microsoft product name on first mention with the short name in parentheses: "Microsoft Intune (Intune)", "Azure Virtual Desktop (AVD)"

Don't repeat product names heavily — after establishing the name, use "the solution", "it", or another pronoun



No-go words and phrases (replace these)

AvoidUse insteadmustimperative verb (Configure... not You must configure...)should"we recommend" (always with the reason) or imperativeutilize, leverage, instantiate, designateuse, create, definee.g."for example"i.e."that is"etc.acceptable only in lists, tables, parentheses, notes, or space-limited contextsad hoc, de factoEnglish equivalent ("industry standard" for de facto)normallyusually, typically, generally, oftenappear (intransitive)"is displayed"showdisplayclickselecttapselect (unless explicitly describing touch input)whitelist / blacklistallowlist / blocklistmaster branchMain branch2FA / two-factor authenticationmultifactor authentication (MFA)log in / log on / login / logonsign in / sign out (two words)highlight, pick (as synonyms for select)select\& (replacing "and")"and" (\& only in UI elements or company/brand names)

Lists



Always introduce a list with a colon

Numbered list: procedure steps

Bulleted list: fields/options from one dialog/menu/pane; single-step procedures

Lower-alpha numbered list: sub-steps within a top-level step

AVOID tables in lesson content (Phrase TMS bloat, Docebo import breaks). Use bold-term definitions, bulleted lists, or numbered procedures instead. Tables only for unavoidable multi-variable comparisons; plain text in cells, no inline formatting.

Punctuation rules:



Incomplete sentence items: no end punctuation

Complete sentence items: period at end

If at least one item is a complete sentence: all items get a period

Exception: no period if all items are 3 words or fewer, or are UI labels/headings/strings

Parallel structure required: if one bullet starts with a verb, all do; if one is a complete sentence, all are







Hyperlinks



Use the article title as the link text. NOT "Learn more", "click here", "find here", "this article".

Add destination context with a vertical bar:



\[Article title | NMM Help]

\[Article title | NME Help]

\[Article title | Microsoft Learn]







Step 4: Apply American English

Non-negotiable for all Nerdio L\&D content. If you've been writing in British/European English, switch.

Spelling differences (key ones)

British / EuropeanAmerican (use this)colourcolorfavouritefavoritebehaviourbehaviorneighbourneighborcentrecentermetre (unit)metertheatretheatercataloguecatalogdialogue (in software UI sense)dialogorganisationorganizationspecialise / specialisedspecialize / specializedanalyse / analysed / analysinganalyze / analyzed / analyzingrecognise / recognisedrecognize / recognizedoptimise / optimisedoptimize / optimizedcustomisationcustomizationauthorisationauthorizationutilise (avoid anyway, see no-go list)(use "use")licence (noun) / license (verb)license (both noun and verb)practice (noun) / practise (verb)practice (both)defencedefenseoffenceoffensetravelling, travelled, travellertraveling, traveled, travelercancelling, cancelledcanceling, canceledlabelling, labelledlabeling, labeledmodelling, modelledmodeling, modeledprogrammeprogramdisc (computing context)diskgreygraytowardstowardamongstamongwhilstwhilelearntlearnedspeltspelleddreamtdreamedburnt (past tense verb)burnedforwards / backwardsforward / backward

Punctuation differences (American style)



Periods and commas go INSIDE quotation marks

Other punctuation (colons, semicolons, question marks unless part of the quote): outside the quotation marks

Date format: May 8, 2026 (month day, year). NEVER 8 May 2026. NEVER 8/5/2026 (ambiguous).

Time format: 9:00 AM / 5:30 PM — uppercase AM/PM, no periods. Or 24-hour for technical contexts.

Decimal point: period (1,024.5). NEVER 1.024,5.

Thousand separator: comma (10,000). NEVER 10 000 or 10.000.



Vocabulary differences (a few that matter for tech writing)

BritishAmericantimetableschedulediary (for software)calendarholiday (vacation sense)vacationflatapartmentliftelevatorpostcodeZIP codemobile (phone)both work in modern US tech writing — use "mobile" or "cell phone"post (mail)mailCVresume

If a phrase sounds idiomatically British when read aloud (e.g., "going forward we shall…", "have a chat about", "fancy a look at", "straight away"), rewrite in plain American English.

Step 5: Self-check before output

Run this checklist before any text is finalized into the deliverable. If any item fails, fix and re-check.



Every product name, feature name, command path, role name, pricing figure, license requirement, version, GA/preview status, launch date has been verified against an authoritative source. URLs noted internally.

American English throughout. No colour, centre, organisation, behaviour, whilst, amongst, 8 May 2026.

No em dashes (—), no en dashes (–). Replaced with comma, period, colon, parentheses, or rewritten.

No exclamation points.

Oxford comma in all series of three or more.

sign in / sign out (two words). No login, log on, log in, signin, etc. unless quoting UI literally.

on-premises — never on-prem or on-premise.

multifactor authentication (MFA) on first mention — never 2FA or two-factor.

All acronyms spelled out on first mention with abbreviation in parentheses.

Numbers: zero–nine spelled out; 10+ as digits; always digits with units.

No click, no tap (unless specifically touch). Use select.

No appear (use is displayed), no show (use display).

No utilize, leverage, instantiate, designate — replaced with simple verbs.

No e.g., i.e.. etc. only in lists/parentheses if space-limited.

No subjective fillers: easy, simple, simply, just, fast, slow, exciting, difficult.

No must / should — replaced with imperative or we recommend.

Second person (you), present tense, active voice. No future tense.

Sentence-style capitalization for headings; title-style only for product/feature/service names.

Nerdio Manager for Enterprise → Nerdio Manager after first mention. NME only in compact contexts (badges, callouts, table cells).

Nerdio is the company, never the product.

Microsoft framed respectfully — never as the problem to be solved.

No invented facts. Every technical claim has a source.



If even one item fails, do not output yet. Loop back and fix.



The never-invent rule

This is the hardest rule and the one that requires real discipline.

If you do not know something with certainty, you DO NOT write it. You either:



Search and verify it, then write it with the source noted, OR

Tell Bas you could not verify it and ask for direction, OR

Leave it out of the deliverable if it is not essential



Things that have been gotten wrong in past lessons by guessing from memory:



Role permission names (the actual Nerdio Manager role might be named slightly differently than what memory suggests)

UI menu paths (the actual order or wording of menu items)

Version numbers and GA dates (memory drifts; check the announcement)

Pricing tiers and what is included in each

License requirements (E3 vs E5 vs E7 — verify, do not guess)

Feature scope (does this feature support that integration? — check the docs, do not assume)

Capitalization of single technical words (App Attach or app attach? — check the source)



If a claim is "approximately right" but you cannot find the exact source, FLAG IT to Bas with the closest source you found. Do not silently round it off into the deliverable.

When flagging an unverified claim to Bas, use this format:



Flagged for verification: "\[the claim]". Closest source found: \[URL]. Suggested action: \[confirm / rewrite / drop]."





Integration with parent skills

From nerdio-microlesson

The microlearning skill provides the visual structure (slide types, fonts, colors, layout, A4 portrait vector PDF). This skill provides the words inside that structure.

Workflow when invoked from nerdio-microlesson:



nerdio-microlesson collects topic + audience Why + slide outline from Bas

Before writing the first cover line, this skill is loaded

This skill runs Steps 1–4 above (identify, verify, style, American English)

Slide content is generated, with every claim verified

This skill runs Step 5 (self-check) on every slide before it is finalized into the HTML

nerdio-microlesson resumes — embeds the verified text into the carousel template

nerdio-microlesson renders to vector PDF as before



The visual specs in nerdio-microlesson are not touched by this skill. Colors, fonts, line spacing, font sizes, layout patterns, iteration recipes — all unchanged. This skill is purely additive.

From nerdio-content

Same pattern but for whatever content type that skill is producing (lesson, ADDIE doc, video script, course description, learner journey, question pool, Docebo copy).

Standalone

When called directly ("check this writing"), the skill runs Steps 3, 4, 5 against the supplied text, plus Steps 1 and 2 for any technical claims it contains. Output: marked-up version with corrections applied + a summary of what was changed and what was flagged for Bas's review.



Bundled reference

The full Nerdio L\&D Style Guide is in the project knowledge as:

nerdio\_style\_guide\_reference\_v3\_md.txt

When in doubt about an edge case (specific abbreviation, specific term, specific punctuation rule), consult that file. The summary in this skill covers the most common rules but is not exhaustive.

For Microsoft writing conventions not covered in either this skill or the Nerdio reference, consult:

learn.microsoft.com/en-us/style-guide

When Nerdio L\&D rules conflict with Microsoft Writing Style Guide rules, Nerdio L\&D wins.



Anti-patterns (what NOT to do)



Don't skip verification because "I'm pretty sure". Memory is wrong often enough to make this rule absolute. The cost of a wrong fact in a published lesson is higher than the cost of a 30-second search.

Don't apply British spelling and assume the spell-checker will catch it. It won't — many words are valid in both, just culturally wrong (e.g., behaviour, analyse, programme).

Don't rewrite Bas's voice. This skill enforces house style and accuracy, not personality. Preserve his cadence, framing, and signature phrasings, per VOICE\_PROFILE\_Bas\_van\_Kaam\_FINAL.md. This skill constrains the words and claims; it does not flatten the register the profile sets.

Don't add "Nerdio recommends..." or "Nerdio believes..." flourishes. Use "We recommend" with the reason, per the style guide.

Don't use em dashes anywhere. Even where they would aid readability. Brand rule.

Don't bluff a step sequence. If you cannot find the exact UI path in NME Help, NMM Help, or Microsoft Learn, flag it to Bas.

Don't trust an AI summary on a third-party site as a source. Authoritative source = vendor's own docs, not someone's blog post about them.

Don't run the self-check at the end of writing all slides at once. Run it slide by slide, sentence by sentence, while the context is fresh.





Version history



May 2026: Skill created. Built on top of nerdio\_style\_guide\_reference\_v3\_md.txt (sourced from WIP-Nerdio\_L\_D\_Style\_Guide.docx Rev 1, Feb 2026, plus Marketing Writing Guidelines, plus Microsoft Writing Style Guide). Standardizes American English. Adds mandatory live verification protocol against Nerdio help docs and Microsoft Learn. Establishes the never-invent rule.

June 4, 2026 (update): Voice/register scope clarified. This skill governs WHAT you say (words, claims, terminology, American English, verified facts), not the register. Register is set per deliverable from VOICE\_PROFILE\_Bas\_van\_Kaam\_FINAL.md (BvK full voice for carousels/LinkedIn/about-Nerdio, Nerdio corporate-warmed for official Docebo lessons/courses/PPT). Profile is loaded alongside this skill before writing, with a mandatory banned-word scan before output. No new style rules added.

