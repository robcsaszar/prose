# Drafting Core Rules

Rules for writing new content. Load when drafting anything longer than 200 words.

---

## Default Voice

Use when no voice sample is provided.

**Style:** Declarative sentences. One idea per sentence. Subject before verb. No throat-clearing.
**Sentence length:** Short-to-medium (10–20 words typical). Occasional short punchy line for emphasis.
**Openings:** Claim or fact first — not "In today's world…" or "It's important to…"
**Endings:** Principle or consequence — not a restatement of what was just said.
**Words to avoid:** leverage, robust, seamless, comprehensive, innovative, impactful, streamline, ecosystem.
**Example tone:** "The deadline moved. That changes what we build first, not whether we build it."

---

## Precedence

When rules conflict:
1. Truth, safety, accessibility, and platform/legal requirements
2. Explicit user instructions
3. Genre and medium norms
4. Rules below

If the user asks for bullets, use bullets. If the medium requires structure, use structure.

---

## Medium Routing

Choose format and register to match the channel, not a global preference.

**Chat / comments / replies / DMs / forum posts:**
- Running prose by default
- Lists only when the information is naturally list-like or the user asked for one
- No decorative formatting or canned support tone
- Prefer straight ASCII quotes and apostrophes (curly quotes read as pasted/auto-formatted text)
- Prefer commas, colons, conjunctions, or full stops over em dashes unless the dash clearly earns its keep

**Email between colleagues:**
- Prose first; lists are fine for discrete items, decisions, or action points

**Documents / specs / reports / technical writing:**
- Structure is expected: headings, bullets, and sequence when they help scanning and precision

**Web pages / help centers / UI text / public docs:**
- Answer or next action goes early
- Preserve scannability and accessibility: descriptive headings, lists for steps, descriptive link text
- Do not flatten useful structure to avoid looking templated

**Long-form posts / articles / criticism / retrospectives:**
- Structure on purpose; pick an angle
- Do not let dates, named milestones, or neat category buckets become the spine unless the user asked for that

---

## Core Rules

### 1. Anchor to the actual context before drafting

Decide what the text is, who it is for, what register it uses, what the reader needs, and — in replies — what specific thread or person it is responding to. A reply that could be pasted into any thread on the same topic reads as generic even if the prose is clean.

### 2. Fit the format to the medium

Over-structuring casual writing makes it feel templated. Under-structuring technical writing makes it harder to use. Format is part of register.

### 3. Prefer concrete specificity over polished generality

Each substantial paragraph should carry at least one concrete anchor:
- A proper noun the reader could look up
- A specific number that is not only a date or version
- A direct quote
- A named decision, moment, or thread
- A checkable detail

What does **not** count:
- "many", "various", "several", "a lot of"
- "in ways that mattered", "meaningful changes", "broad implications"
- "the standard X arc", "the usual pattern", "as is often the case"
- Vague intensifiers in place of claims: "essentially", "fundamentally", "ultimately"
- Milestone names, dates, or feature labels standing alone with no material consequence attached

If the most concrete thing in a paragraph is a name and a date, the paragraph is still probably too generic.

### 4. Specificity must be earned

Prefer fewer verified facts over many guessed ones. Do not use specificity theater:
- Invented milestone names or synthetic quotes
- Suspiciously exact claims that cannot be sourced
- Hidden-mechanism claims (internal logic, unseen motives, back-end behavior) presented as fact

If you cannot verify a claim, attribute it, soften it, or cut it.

### 5. Use plain words; allow ordinary repetition; prefer verbs

Do not chase synonyms for basic words like "problem", "change", "system", "work", or "people".
Repeat the ordinary word when it is the right word.

Prefer:
- "we changed it" → not "the implementation of the change"
- "latency dropped" → not "a reduction in latency was observed"
- "applying the rule" → not "the application of the rule"

Prefer actions happening to people over abstractions being observed by systems.

### 6. Cohere through reference and sentence shape

Use pronouns and continued reference when the reader can track them. Do not restate the full frame in every paragraph. Treat "Furthermore", "Moreover", "Additionally", "Importantly", "Notably" as things to justify, not default sentence starters.

A period should mark a real pause, shift, or emphasis — not merely the place where an adjacent thought arrived.

**Combining related thoughts:**
- "The term works. It names the pattern." → weaker
- "The term works: it names the pattern." → stronger (carries the relationship)

Do not turn every idea into its own sentence for crispness.

### 7. Do not perform

Avoid keynote cadence, mission-statement phrasing, and applause-line endings. Also avoid:
- "Great question", "Absolutely", "That's an excellent point"
- "I hope this helps", "Feel free to reach out"
- Canned praise or canned closers unless the situation clearly calls for them

Start where the answer starts. Stop where the answer stops.

### 8. Calibrate confidence, stance, and voice to genre

Be confident where evidence is strong. Be explicit where it is weak or interpretive.

- If the genre normally carries a visible writer (review, opinion, comment), let the writer appear
- If the genre normally aims at neutrality (summary, docs, news), do not inject attitude or first person
- Do not manufacture a view when the subject does not require one
- Do not sand everything to polite neutrality when the subject naturally invites a view

### 9. Show concrete things before generalizing

Do not open with abstract diagnosis when the reader has nothing concrete to attach it to. Exception: in web, docs, email, and task-oriented writing, leading with the conclusion is fine if the conclusion is concrete enough to be useful.

Preferred order:
1. What happened
2. Where the pattern appeared
3. What constraint mattered
4. What failed or changed
5. What that seems to mean

### 10. Watch regularity

Suspect: when the most visible feature of the writing is its own regularity.

Watch for:
- Parallel enumeration and reflexive three-part cadence inside sentences
- Multiple sentences doing hidden list work without bullets
- Concession-plus-positive rhythm ("not X, but Y")
- Paragraph-closing type definitions ("the kind of X where Y")
- Identical paragraph arcs
- The same punctuation move in every paragraph
- Stacked mini-sentences for impact where each sentence carries one adjacent thought

Three-item parallel lists still count as regularity. The fix is to break the repeated pattern, not just vary the count.

### 11. Let the thought develop

Longer pieces should not feel pre-solved. Let the thought develop through a concrete example, a noticed detail, or a brief doubling-back when the material allows it.

Development can happen inside a sentence. A cumulative sentence starts with the main claim and adds the reason, qualification, or consequence that belongs with it.

### 12. Choose structure consciously for longer pieces

Default genre shapes are not wrong — they are only a problem when used by reflex.

For task pages, procedures, reference docs, news briefs: predictable structure is often the clearest. Do not avoid it for novelty.

For retrospectives, criticism, feature writing, and developmental pieces — avoid these defaults unless the user asked for them:
- Starting state → changes → verdict
- One topic bucket per paragraph
- One paragraph per named milestone

Choose a through-line instead: one complaint that stopped mattering, one system that changed the rest, one shift in what people actually had to do.

Useful alternatives: thematic, reverse-chronological, perspective-led, counterfactual, opinion-first, single-example-led.

### 13. Do not make catalog prose or system-tour prose

**Catalog prose:** paragraph mainly names milestones, categories, feature nouns, or system labels. Fix: pick one change and trace its consequence.

**System-tour prose:** each paragraph can be summarized with a single label (background, mechanism, impact, response, ending). Fix: cross-wire paragraphs so they depend on each other instead of sitting like labeled boxes.

### 14. Revise by reading and cutting

Re-read as a first-time reader. Cut:
- Anything that is auditioning
- Sentences whose only job is to announce the next sentence
- Paragraphs that restate each other

Replace the most generic clause with something specific, or delete it. Most edits should make the text shorter — but do not confuse concision with chopping. Combining two tightly related sentences is sometimes the cleaner edit.

---

## Structural Techniques (Posts and Articles)

### Start with the punchline

For most post types: lead with the specific insight, not the journey to it.

❌ "In this article, we'll explore the challenges of migrations..."
✅ "Codemods automate 70% of migrations. Here's how to get to 95%."

### Use subheadings as scannable statements

❌ `## Introduction` / `## Background` / `## Results`
✅ `## Why docs go stale` / `## What codemods miss` / `## The real fix`

### Show, don't just tell

Code examples, performance numbers, expected output, concrete steps. If you can't picture it happening in real life, rewrite it.

❌ "The conversion process is simple and efficient."
✅ "Here's the conversion: `$ prpm install @nextjs/migration` — 47 files migrated in 90 seconds, 3 flagged for manual review."

### Honest limitations earn trust

❌ "Our comprehensive solution handles all use cases."
✅ "This won't catch dynamic imports. You'll need to fix those manually — expect about 5% of files."

### End with action, not summary

❌ "In conclusion, we've discussed how X works and why it's useful."
✅ A specific CTA, a challenge, an open question, or the actual next step.

---

## Safety Rails

These are not AI tells by themselves: em dashes, semicolons, "however", competent punctuation, and the right word even if it appears on somebody's banned list.

Do not:
- Invent typos
- Break grammar on purpose
- Inject slang, profanity, fake uncertainty, or staged messiness to simulate humanity
- Alternate sentence lengths by formula
- Remove needed structure in the name of sounding less AI-written
