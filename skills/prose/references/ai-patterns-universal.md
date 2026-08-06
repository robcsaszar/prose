# AI Patterns — Universal

Apply to ALL content types regardless of channel. Flag every instance with exact quote and location.

**Structure outweighs vocabulary.** A 2026 study of 61,608 human- and model-written texts (University of Maryland / Google DeepMind, arXiv:2604.03136) found that surface-editing AI text — removing clichés and purple prose — barely moved a classifier reading only structural features: detection dropped from 95.5% to 93.9%. The durable signal is construction, not diction: the moral stated at the end of every paragraph, the single-track claim-support-takeaway shape, the tidy endings. Word-level tells also expire on their own ("delve" peaked in 2023–2024 and collapsed in 2025; newer models suppress em dashes), while structural habits persist across model generations. Fixing Part 1 without fixing Parts 2 and 5 produces text that still reads as AI.

---

## Part 1: Phrase-Level Markers

### AI vocabulary words

Flag when used as fallback diction (not when they are plainly the right word):

`actually`, `additionally`, `align with`, `albeit`, `boasts`, `certainly`, `comprehensive`, `crucial`,
`cultivate`, `delve`, `elevate`, `empower`, `enable`, `enduring`, `enhance`, `essentially`,
`ever-changing`, `ever-evolving`, `ever-growing`, `facilitate`, `foster`, `fundamental`, `garner`,
`game-changing`, `groundbreaking`, `harness`, `highlight` (verb), `holistic`, `innovative`,
`interplay`, `intricate` / `intricacies`, `journey`, `key` (adjective), `landscape` (abstract noun),
`leverage` (verb), `multifaceted`, `navigate` (metaphor), `next-gen`, `nuanced`, `overall` (filler qualifier),
`paradigm`, `pivotal`, `profound`, `realm`, `robust`, `seamless`, `showcase`, `streamline`, `superpower`,
`synergy`, `tapestry` (abstract noun), `testament`, `transformative`, `typically`, `underscore` (verb),
`unlock`, `unveil`, `utilize`, `valuable`, `various` (vague pluralizer), `vibrant`, `whilst`

The problem is repeated fallback diction, not the existence of any one word.

Shelf-life warning: this list decays. Each model generation retires the previous tells ("delve" is GPT-4-era; "align with", "enhance", "fostering" are GPT-4o-era; "emphasizing", "highlighting", "showcasing" persist into later generations). Treat individual words as hints and the underlying habits — inflation, hedging-by-template, copula avoidance — as the actual target. A synonym of a listed word is not itself suspect; the list is literal.

### Hollow intensifiers

`crucial`, `essential`, `incredibly`, `significantly`, `vital` — when used without evidence.

### Promotional and advertisement-like language

**Before:** "Nestled within the breathtaking region of Gonder, the town stands as a vibrant destination with rich cultural heritage and stunning natural beauty."
**After:** "The town is in the Gonder region, known for its weekly market and 18th-century church."

Watch for: `boasts a`, `vibrant`, `rich` (figurative), `profound`, `enhancing its`, `nestled`, `in the heart of`, `groundbreaking`, `renowned`, `breathtaking`, `must-visit`, `stunning`

### Undue emphasis on notability and media coverage

**Before:** "Her views have been cited in The New York Times, BBC, Financial Times, and The Hindu. She maintains an active social media presence with over 500,000 followers."
**After:** "In a 2024 New York Times interview, she argued that AI regulation should focus on outcomes rather than methods."

Watch for: a list of outlets or credentials with no context for any single one, `active social media presence`, `independent coverage`, `written by a leading expert`. Naming a source is fine; stacking sources as proof of importance is not.

### Copula avoidance

**Before:** "Gallery 825 serves as LAAA's exhibition space for contemporary art. The gallery features four separate spaces and boasts over 3,000 square feet."
**After:** "Gallery 825 is LAAA's exhibition space for contemporary art. The gallery has four rooms totaling 3,000 square feet."

Watch for: `serves as` / `stands as` / `marks` / `represents [a]` / `boasts` / `features` / `offers [a]` substituted for a plain `is`, `are`, or `has`. Also `refers to` in a lead definition ("X refers to the practice of...") — a definition should read "X is...". The elaborate construction rarely adds information.

### Vague attributions and weasel words

**Before:** "Experts believe it plays a crucial role in the regional ecosystem."
**After:** "It supports several endemic fish species, according to a 2019 survey by the Chinese Academy of Sciences."

Watch for: `industry reports`, `observers have cited`, `experts argue`, `some critics argue`, `several sources suggest`, `research shows` (without naming the research), `many believe`

### Overgeneralized sourcing

Inflating the count: one review becomes "reviewers note"; two articles become "widespread coverage"; a short list of examples gets an implied "and many more" the sources never supported.

**Before:** "Reviewers praised the interface, and the launch received extensive media coverage."
**After:** "One reviewer (TechRadar, March 2025) praised the interface; two trade outlets covered the launch."

Keep the count honest: "one reviewer", "two trade articles", the actual names. `such as` implying a longer list, `multiple outlets` with one citation, and trivial mentions inflated into `has been featured in` all count.

### AI phrasing and metaphors

Replace these with language specific to what is actually being said:

- "brutal clarity" / "painfully clear" / "blunt honesty"
- "laying the groundwork" / "launching a new chapter"
- "the energy in the room"
- "Here's to [noun]!" / "will never be the same" / "ends the era of"
- "not only...but also" (parallelism to simulate thoroughness)
- "here's a breakdown" (cut it, just give the breakdown)
- "in the ever-evolving landscape" / "in today's fast-paced world" (filler openers with no information)
- "a testament to" (gestures at quality without specifying)
- "there is a specific kind of [magic/energy/power] that happens when" (vague wonder-framing)
- "Below is..." / "Below:" as a list introduction (cut the intro, start the list)
- "such as" repeated as the only connector when introducing examples

### Filler openers

Just state the thing. Cut the runway.

- "In today's [noun]..."
- "When it comes to..."
- "At the end of the day..."
- "The truth is..." (before a generic claim)
- "It's important to note that"
- "It's worth noting that"
- "Let's dive into..."
- "Without further ado..."
- "In order to achieve this goal" → "To achieve this"
- "Due to the fact that" → "Because"
- "At this point in time" → "Now"
- "It is important to note that the data shows" → "The data shows"
- "The system has the ability to process" → "The system can process"

### Hedge phrases

**Before:** "It could potentially possibly be argued that the policy might have some effect on outcomes."
**After:** "The policy may affect outcomes."

Watch for: `One might argue`, `It goes without saying`, `I was wondering if perhaps`, `Would it be possible to maybe`

### Overused transitions

Justify before using: `Furthermore`, `Moreover`, `Additionally`, `Importantly`, `Notably`, `In conclusion`

### Undue emphasis on significance and legacy

**Before:** "This marked a pivotal moment in the evolution of regional statistics in Spain, reflecting broader movements to decentralize administrative functions."
**After:** "The institute was established in 1989 to publish regional statistics independently from the national office."

Watch for: `stands as`, `serves as a testament`, `vital role`, `underscores its importance`, `reflects broader`, `symbolizing its enduring`, `setting the stage for`, `represents a shift`, `key turning point`, `indelible mark`, `deeply rooted`

### Superficial analyses with -ing endings

**Before:** "The color palette resonates with the region's natural beauty, symbolizing local landscapes and reflecting the community's deep connection to the land."
**After:** "The architect said the colors were chosen to reference local bluebonnets and the Gulf coast."

Watch for: participial phrases tacked onto sentences to add fake depth — `highlighting...`, `underscoring...`, `symbolizing...`, `reflecting...`, `contributing to...`, `cultivating...`, `showcasing...`

### Unsupported causality

Weaken when the evidence only supports sequence or correlation, not cause:

`drove`, `proved`, `showed that`, `made clear that`, `tracked with`, `led directly to`, `caused` (when unverified)

Use instead: `coincided with`, `appeared alongside`, `was followed by`

---

## Part 2: Structural Markers

### Generic openings

Flag if the piece opens with an abstract diagnosis when the reader has nothing concrete to attach it to:
- No specific story, example, or contrarian take
- A vague general claim that could open any article on the same topic

### Catalog prose and system-tour prose

**Catalog prose:** paragraph mainly names milestones, categories, or feature labels. No consequence, no argument.

**System-tour prose:** each paragraph maps to a clean label (background, mechanism, impact, response, ending). Paragraphs sit like labeled boxes instead of depending on each other.

Fix for both: pick one change and trace its consequence. Cross-wire the piece.

### Outline-like "Challenges and Future Prospects" sections

**Before:** "Despite its prosperity, the area faces challenges typical of urban areas. Despite these challenges, it continues to thrive."
**After:** "Traffic congestion increased after three new IT parks opened in 2015. The municipal corporation began a stormwater drainage project in 2022."

### Uniform paragraph length

If nearly all paragraphs land at the same length, the writing looks pre-computed. Vary one.

### Emotion rendered as body metaphor

AI renders feeling through stock physical sensation at roughly twice the human rate (81% vs 38% of texts in the 2026 UMD/DeepMind corpus): "a tightening in the chest", "the team felt the blow", "her stomach dropped". Human writing more often names the event and its cost.

**Before:** "The layoff announcement hit the team like a punch to the gut."
**After:** "Three of the eight engineers handed in notice within the week of the announcement."

Not a ban on physical description — flag it when the body metaphor is generic and stands in for a nameable fact or consequence.

### Stating the moral (pre-digested conclusions)

Ending the story with its lesson, the paragraph with its meaning, the section with its recap — AI does this in 77% of texts vs 52% for humans. If the point has been shown, it does not need to be named. Delete the paragraph's last sentence and check: the text almost always got better.

### The outline test

Read the first sentence of every paragraph in order. If they form a clean standalone summary of the piece, the document-level structure is machine-shaped: one neat claim per paragraph, orderly elaboration under each. Reorder, merge, or start one section somewhere unexpected — mid-thought, on a detail, on an objection. (Exempt: specs, runbooks, executive summaries, and other formats where an outline is the point.)

### Regularity patterns

Watch for:
- Reflexive three-part parallel cadence inside sentences (X, Y, and Z — by formula)
- Multiple sentences doing hidden list work without bullets
- Concession-plus-positive rhythm by reflex: "not X, but Y" / "may sound X, but Y"
- Paragraph-closing type definitions: "the kind of X where Y"
- Identical paragraph arcs
- One neat claim at the top of every paragraph followed by orderly elaboration
- The same punctuation move in every paragraph

Three-item parallel lists still count as regularity even when the count varies to four.

### Stacked fragment cadence

"X. Y. Z." format used as punchlines. Rewrite as a real sentence unless the break creates genuine emphasis.

**Before:** "Speed matters. Users notice. The business suffers."
**After:** "Speed matters: users who hit a slow page leave, and the business sees it in conversion."

### Three-part parallel structure

"It's not about X. It's about Y. It's about Z." → Rewrite as one direct sentence.

### Rule of three overuse

Distinct from the negation cadence above: this is forcing an unrelated list into exactly three items to appear comprehensive, not a rhetorical "not X, it's Y" construction.

**Before:** "The event features keynote sessions, panel discussions, and networking opportunities. Attendees can expect innovation, inspiration, and industry insights."
**After:** "The event includes talks and panels. There's also time for informal networking between sessions."

### Summary conclusions

**Before:** "In this post, we've explored how X works, discussed Y, and shown why Z matters."
**After:** A challenge, a principle, an open question, or the actual next step.

### Vague generic conclusions

**Before:** "The future looks bright. Exciting times lie ahead as the company continues its journey toward excellence."
**After:** "The company plans to open two more locations next year."

### Self-posed question as transition

"Why? Because..." → Rewrite as a declarative statement.

### Runway sentences

A vague hype line before the actual specific detail. Cut the runway, start with the substance.

---

## Part 3: Style Patterns

### Em dashes and en dashes

No em dashes (—) or en dashes (–) in the final output. Also catch spaced variants (` — `) and double hyphens (` -- `).

Replace with, in order of preference:
- A period (start a new sentence)
- A comma (tight aside)
- A colon (introducing an explanation)
- Parentheses (a true aside)
- Restructure the sentence

**Before:** "The term is primarily promoted by Dutch institutions—not by the people themselves—even in official documents."
**After:** "The term is primarily promoted by Dutch institutions, not by the people themselves, and it appears even in official documents."

Scan the final output for `—` and `–`. Any hit means the draft is not done.

**Creative channel exception.** In fiction, scripts, and poetry, the dash marks interrupted speech and broken thought, and no other punctuation does that job: `"I told you—" she stopped.` A period ends the line, a comma joins it, and both lose the interruption. Keep dashes inside dialogue and in verse where the break is the effect. Outside dialogue, in the narration itself, the rule holds.

### Overuse of boldface

**Before:** "It blends **OKRs**, **KPIs**, and **the Business Model Canvas**."
**After:** "It blends OKRs, KPIs, and the Business Model Canvas."

Do not bold for emphasis by default. Bold only when it materially aids scanning.

### Inline-header vertical lists

**Before:**
> - **User Experience:** The UX has been significantly improved.
> - **Performance:** Performance has been enhanced.

**After:** "The update improves the interface and speeds up load times."

### Title case in headings

**Before:** `## Strategic Negotiations And Global Partnerships`
**After:** `## Strategic negotiations and global partnerships`

Sentence case by default. Title case only when the medium convention requires it.

### Emojis

No emojis in headings or as bullet-point decorations in prose contexts. Keep only when they carry genuine meaning in the medium (e.g., IM reactions, social media shorthand).

### Curly quotation marks in plain-text contexts

In chat, comments, casual Markdown, and text typed directly into editors: prefer straight ASCII quotes. Curly quotes read as pasted or auto-formatted.

### Passive voice

Rewrite when active voice makes the sentence clearer and more direct.

**Before:** "No configuration file needed. The results are preserved automatically."
**After:** "You do not need a configuration file. The system preserves the results automatically."

### Negative parallelisms and tailing negations

**Before:** "It's not just about the beat riding under the vocals; it's part of the aggression."
**After:** "The heavy beat adds to the aggressive tone."

Clipped tailing-negation fragments: **Before** "The options come from the selected item, no guessing." **After** "The options come from the selected item without forcing the user to guess."

### Hyphenated word pair overuse

Hyphenate compound modifiers before the noun; open after the noun (especially after a linking verb).

✅ Attributive (before noun): `a high-quality report`, `a cross-functional team`, `a long-term plan`
✅ Predicative (after noun): `the report is high quality`, `the team is cross functional`
✗ `The report is high-quality` / `The team is well-known` (predicative over-hyphenation)
✗ `-ly` adverb compounds: `highly-qualified`, `newly-designed` (never hyphenate `-ly` adverbs)
✗ Reflexive `ever-` compounds: `ever-changing`, `ever-evolving`

Keep hyphens when they prevent ambiguity or when the term is conventionally hyphenated: `state-of-the-art`, `cost-effective`.

### Elegant variation (synonym cycling)

**Before:** "The protagonist faces many challenges. The main character must overcome obstacles. The central figure eventually triumphs. The hero returns home."
**After:** "The protagonist faces many challenges but eventually triumphs and returns home."

Repeat the ordinary word when it is the right word.

### False ranges

**Before:** "Our journey has taken us from the Big Bang to the grand cosmic web, from star formation to dark matter."
**After:** "The book covers the Big Bang, star formation, and current theories about dark matter."

---

## Part 4: Communication and Framing Patterns

### Sycophantic and servile tone

**Before:** "Great question! You're absolutely right that this is a complex topic."
**After:** "The economic factors you mentioned are relevant here."

Watch for: `Of course!`, `Certainly!`, `You're absolutely right!`, `I hope this helps`, `Let me know if you'd like`, `Here is a...`

### Collaborative communication artifacts

Strip before delivering content: "Here is an overview. I hope this helps! Let me know if you'd like me to expand on any section." → Just give the overview.

### Knowledge-cutoff disclaimers and speculative gap-filling

**Before:** "While specific details are not extensively documented in readily available sources, it appears to have been established sometime in the 1990s."
**After:** "The company was founded in 1994, according to its registration documents."

**Before:** "Information about her early life is not publicly available, suggesting she maintains a low profile."
**After:** "Her early life is not documented in the available sources." (or omit the section)

### Persuasive authority tropes

Cut the ceremony before a claim that would stand on its own.

**Before:** "The real question is whether teams can adapt. At its core, what really matters is organizational readiness."
**After:** "The question is whether teams can adapt. That mostly depends on whether the organization is ready to change its habits."

Watch for: `The real question is`, `at its core`, `in reality`, `what really matters`, `fundamentally`, `the deeper issue`, `the heart of the matter`

### Aphorism formulas

Turning an ordinary claim into a reusable-sounding aphorism that sounds profound without adding precision. Replace the formula with the concrete claim it gestures at.

**Before:** "Symmetry is the language of trust. Efficiency becomes a trap when teams forget the human layer."
**After:** "Symmetric layouts often feel more predictable to users. Teams can over-optimize workflows and miss how people actually use them."

Watch for: `X is the Y of Z`, `X becomes a trap`, `X is not a tool but a mirror`, `the language of`, `the currency of`, `the architecture of`.

### Conversational rhetorical openers

A fake-candid hook manufacturing intimacy before an ordinary point. The tell is the theatrical pause-and-reveal: a one-word question or aside, then the "real" answer. A person being honest usually just says the thing.

**Before:** "Is it worth the price? Honestly? It depends on how often you'll use it."
**After:** "Whether it's worth the price depends on how often you'll use it."

Watch for: `Honestly?`, `Look,`, `Here's the thing`, `The thing is`, `Let's be honest`, `Real talk` used as standalone hooks. Not a tell when these appear mid-sentence in ordinary casual writing — see Part 6.

### Signposting and announcements

**Before:** "Let's dive into how caching works. Here's what you need to know."
**After:** "Next.js caches data at multiple layers, including request memoization, the data cache, and the router cache."

Watch for: `Let's dive in`, `let's explore`, `let's break this down`, `here's what you need to know`, `now let's look at`

### Diff-anchored writing

Documentation or comments written as if narrating a change rather than describing the thing as it is. Unless the document is inherently version-scoped (changelog, release notes, migration guide), it should read coherently without knowing what changed last.

**Before:** "This function was added to replace the previous approach of iterating through all items, which caused O(n²) performance."
**After:** "This function uses a hash map for O(1) lookups, avoiding the O(n²) cost of naive iteration."

### Fragmented headers

A heading followed by a one-line paragraph that simply restates the heading before the real content begins.

**Before:**
> ## Performance
> Speed matters.
> When users hit a slow page, they leave.

**After:**
> ## Performance
> When users hit a slow page, they leave.

### Standalone hype fragments

"This is big." / "Game changer." → Cut or replace with a specific claim.

---

## Part 5: Second-Order Tells — "Clean Slop" (Model House Style)

What edited AI looks like after a cleanup pass: the Part 1 vocabulary is gone, yet every sentence is load-bearing, every paragraph sticks the landing, and nothing ever relaxes. No human sustains that. Each move below is fine on its own; stacked through a whole text, they form a second, subtler uniform. Check for these AFTER the Part 1–4 patterns are fixed — they are what the fixes tend to produce.

### Uniform confidence

No sentence in the whole text is unsure of itself. Human confidence is uneven because knowledge is: hedges sit on the actual soft spots ("probably", "I think", "we'll see"), and plain flat statements sit where the writer is sure. AI hedging is either absent or smeared over everything as insurance. Flag a text where every claim lands with identical certainty.

### Uniform maximum punch (no slack)

Every sentence squeezed for effect, every paragraph closing on a beat. A person's attention is uneven and honest prose shows it: one or two sentences per text are allowed to be ordinary — an aside that trails off, a flat statement, a "we'll see". Slack is not a staged typo or an inserted "um"; those are props. It is letting an ordinary sentence be ordinary.

### Aphorism budget exceeded

One punchy one-liner closing a paragraph is an accent. An aphoristic close on paragraph after paragraph is a metronome. Budget: at most one per text; demote the rest to plain statements.

### Upgraded negative parallelism

"That's not X. That's Y." — the negative parallelism from Part 1, rebuilt as two clipped sentences to survive the cleanup. Same fix: say what Y is and never mention X.

### Balanced antitheses replacing banned triads

"Readers discount the cliché; they believe the invented fact" is fine once. Three of these see-saw constructions per text is the rule of three wearing a new coat.

### Clipped fragment pairs for drama

"Merged. One motion." "One team, one pulse." Two-beat fragments standing in for the stacked-fragment cadence flagged in Part 2.

### Verdict verbs

Studies "quietly kill", findings "demolish", data "buries" a claim. Dramatization compressed into a single verb. Calmer: "contradicts", "weakens", "suggests otherwise".

### Recycled hooks

`The real question is`, `Here's what that means in practice`, `Here's the thing`, `The part that got me:` — replacement phrases that became tells themselves.

### Replacement tics

Any substitute phrase repeated across three texts becomes a marker in its own right, whatever the phrase is. A worn phrase is rarely fixed by a fresher phrase — most of the time the right replacement is nothing: delete the framing and lead with the substance. When a review finds one, add it to this section or the formula watchlist, and add a scanner rule if it is mechanical.

### Document-level template

Hook, numbered evidence, a turn ("So I built..."), one qualifier, closing question — the whole piece poured into a product-announcement mold regardless of content. Catch it with the outline test (Part 2). Break it by starting one section in the middle of a thought.

---

## Part 6: What NOT to Flag (False Positives)

A clean human writer can hit several patterns above without any AI involvement. Do not rewrite legitimate prose. The following are NOT reliable indicators on their own:

- **Perfect grammar and consistent style** — many writers are professionals or have been edited
- **Mixed casual and formal registers** — often a person in a technical field or with neurodivergent prose habits
- **"Bland" or "robotic" prose** — AI prose has *specific* tells; generic dryness without those tells is just dry writing
- **Formal or academic vocabulary** — AI overuses *specific* words (see vocabulary list above), not all fancy words
- **Em dashes alone** — many editors and journalists use them often; evidence only when paired with formulaic rhythm
- **Curly quotes alone** — macOS, Word, and most CMSes auto-curl by default
- **Common transition words in isolation** — one "however" is not a tell; it's a tell when piled up
- **Unsourced claims** — most of the web is unsourced; lack of citations doesn't prove anything
- **Letter-style opening or closing** — salutations and sign-offs predate ChatGPT by centuries
- **One short emphatic sentence** — humans use clipped sentences to land a point; flag stacked-fragment cadence only when several short fragments appear in a row and inflate the tone
- **"Honestly" or "look" mid-sentence** — ordinary in casual writing; the tell is the standalone theatrical opener (see Conversational rhetorical openers in Part 4), not the word itself
- **Correct, complex formatting** — visual editors and templates produce clean output without any AI involvement
- **Secondhand text** — do not rewrite watched phrases inside quotations, titles, proper names, or examples where the phrase is being discussed rather than used
- **Fixed strings** — code, commands, flags, identifiers, file paths, product names, error messages, legal phrasing, and defined terms are not prose. A watched word inside one of them is part of the string, and changing it breaks the thing it names
- **Craft in the creative channel** — fragments, repetition, intentional ambiguity, and a character who talks in stock phrases are all deliberate in fiction, scripts, and poetry. Judge them against the effect they produce, not against a pattern list. Dialogue in particular is allowed to sound like a person with verbal tics, because people have them
- **The uniform shape of a procedure** — matching paragraph lengths, steady sentence rhythm, and unvarying confidence are what make a runbook followable. In documentation these are the target, not the tell

When in doubt, look for clusters of tells, not isolated ones. A single em dash means nothing; an em dash plus rule-of-three plus `vibrant tapestry` plus a "Challenges and Future Prospects" section is a confession.

---

## Part 7: Signs of Human Writing (Preserve These)

When you see these, lean toward leaving the prose alone. They are evidence of a real person writing, and over-editing will destroy what makes the piece sound human.

- **Specific, unusual, hard-to-fabricate detail** — a real address, a weird quote, "the lawyer who used to work upstairs from my dentist." LLMs round off specifics; humans hoard them.
- **Mixed feelings and unresolved tension** — "I think this is mostly good, but it bothers me, and I can't fully explain why." LLMs default to clean takes.
- **Dated, era-bound references** — slang, memes, or in-jokes that map to a specific year and subculture.
- **First-person editorial choices the writer can defend** — if the writer can explain why they made a particular cut or word choice, that's a strong human signal.
- **Variety in sentence length** — real writing alternates short and long; AI writing tends toward an even, mid-length cadence.
- **Genuine asides, parentheticals, or self-corrections** — "(I keep wanting to say 'almost' here, but it really was certain.)" Models rarely interrupt themselves like this. A correction left visible mid-paragraph ("Or rather, we had the idea but didn't see what it meant") is honest and human — once per text, where a real correction happened.
- **Plain copulas and plain verbs** — "is", "has", "wrote", "moved", "used", "tried", "died". AI dodges these for elevated substitutes; humans use them freely. Never "fix" a plain verb into a fancier one.
- **Superlatives and intensifiers when true** — "the first", "the only", "one of the best", "very", "perhaps", "tends to". These read as honest when they are; do not sand them off as hype without checking whether they're simply accurate.
- **Hedges sitting on real soft spots** — "probably", "I think", "still a hypothesis" attached to the exact claim that is uncertain. Uneven confidence is a human signal (see Part 5, Uniform confidence); do not flatten it.
- **Direct address of the reader** — human writing treats the audience as present ("you") at four times the AI rate in posts, essays, and docs. Where the genre allows it, "you" is normal; do not depersonalize it away.
- **Slack sentences** — "We'll see." "Or not, I don't know." One or two ordinary, unforced sentences are what thinking sounds like on the page, not filler to cut.
