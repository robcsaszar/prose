---
name: prose
description: >
  Comprehensive writing skill for drafting, revising, and humanizing prose in two modes.
  (1) DRAFT MODE — write new content in the correct voice and structure for the medium;
  (2) REVIEW MODE — scan existing text for AI writing patterns, score it, and rewrite
  in an authentic human voice. Auto-detects channel (Blog, social media, Email, IM) and
  applies channel-specific rules. Supports voice calibration from a writing sample.

  Use when writing blog posts, articles, documentation, emails, social media posts,
  IM, marketing copy, or UI text. Also use when reviewing a draft
  for AI texture, humanizing AI-generated writing, checking if text sounds like AI,
  rewriting in a specific voice, or removing AI patterns.

  Trigger phrases are humanize, sounds like AI, voice check, blog review,
  rewrite in my voice, social media post review, email review,
  write a blog post, draft this, remove AI patterns, AI detection,
  write an email, write a social media post.

  Not for code comments, commit messages, or private notes.
---

# Writing

Two modes. Detect the correct one before doing anything else.

## Mode Detection

**Draft mode** — user has a topic, brief, or outline and wants new content written.
**Review mode** — user has existing text and wants it improved, humanized, or scored.

If ambiguous: ask — "Do you want me to write new content, or review/rewrite something you already have?"
If the user does not respond, default to Draft Mode.

---

## Voice Calibration

Before drafting or rewriting, ask for a voice sample if the user hasn't provided one.
For short-form targets (IM, emails under 200 words): skip voice calibration unless the user has already provided a sample.

> "Share 1–3 paragraphs of your own writing that feel most like you. I'll match your
> sentence rhythm, word choice, and structural habits."

Analyze the sample for:
- Sentence length tendency (punchy / analytical / mixed)
- How they open (claim-first, story-first, data-first, context-first)
- Punctuation habits (parentheticals, colons, semicolons)
- Recurring phrases or verbal tics
- How they end (principle, challenge, open question, action)
- Words they never use

If no sample: proceed with the default voice — see `references/drafting-core.md` § "Default Voice". For blog, essay, opinion, or personal writing, also see `references/personality-and-soul.md` — a clean default voice can still read as soulless without it.

---

## Draft Mode

### Phase 0 — Understand before writing

Ask before drafting:
1. What does the reader need to do or feel after reading? *(determines medium and audience fit)*
2. What would actually surprise this reader — what do they already think they know that's incomplete?
3. What is the single job of this text — inform, persuade, instruct, entertain, or convert?
4. What register fits the context — formal, casual, technical, conversational — and will it stay stable?
5. **Through-line** — one concrete example, case, or consequence that can carry real weight

If task-oriented: answer or next action goes first.
If long-form: pick the through-line and one concrete anchor before drafting.

Before drafting, ask: what is the one concrete example or consequence that could carry this piece? If you can't name it, you are not ready to draft.

MANDATORY READ before drafting anything longer than 200 words:
→ [`references/drafting-core.md`](references/drafting-core.md) — core rules and medium-specific patterns

Do NOT load `references/ai-patterns-universal.md` during drafting — it is for review only.

### Phase 1 — Draft

Write to fit the actual context, not an abstract ideal of "good writing."

Active principles:
- Each substantial paragraph carries at least one concrete anchor (proper noun, specific number, direct quote, named decision, checkable detail). *For blog, article, and social media. For IM and short email: one anchor per message suffices.*
- No vague claims: "many", "various", "broad implications", "meaningful changes" fail the anchor test
- Use plain words; repeat the ordinary word when it is the right word; prefer verbs over nominalizations
- Keep register stable; match format to medium

### Phase 2 — Revise

MANDATORY: Run required checks after drafting.
→ [`references/required-checks.md`](references/required-checks.md)

If the piece still feels off after required checks (longer work only):
→ [`references/long-form-diagnostics.md`](references/long-form-diagnostics.md)

When revision examples would help:
→ [`references/examples.md`](references/examples.md)

---

## Review / Humanize Mode

Do NOT load `references/drafting-core.md` during Review/Humanize Mode — it is for drafting only.

### Step 0 — Auto-detect content type

Classify the channel before running any checks. State the detection at the top of the review.

**Email** — has: subject line / greeting formula (Hi Name, Dear Name) / explicit ask + sign-off structure
**social media** — has: one-sentence-per-line throughout / hashtags / engagement CTA at end / under 3,000 chars with no headings
**IM** — has: @mentions / channel refs / casual tone / under 500 chars / no greeting or sign-off
**Blog post** — has: headings / 3,000+ chars of structured prose / multiple developed paragraphs

If one channel matches clearly: state the detection and proceed.
If ambiguous (signals conflict or none fire): ask — "What format is this? Blog post, social media, Email, or IM?" Do not proceed until answered.

### Step 1 — AI pattern scan

MANDATORY READ — universal markers first:
→ [`references/ai-patterns-universal.md`](references/ai-patterns-universal.md)

Then load channel-specific markers:
→ [`references/ai-patterns-channels.md`](references/ai-patterns-channels.md)

Apply universal markers to ALL content. Apply channel-specific markers only for the detected type.
List every flagged item with the exact quote and its location.

### Step 2 — Originality check

Flag if the content:
- Could have been written by anyone with a search engine (no earned authority, no specific experience)
- Has no firsthand experience, customer story, or concrete evidence anywhere
- Makes the same point twice without adding depth
- Recycles industry framing ("the future of X is Y")
- Missing the "only I could write this" factor

social media extra: flag product plugs dressed as lessons; personal stories with fortune-cookie takeaways.

### Step 3 — Score

MANDATORY READ for scoring dimensions per channel:
→ [`references/channel-rules.md`](references/channel-rules.md)

Provide a one-sentence justification for each score.
If AI-Likeness is low but Domain Credibility / Clarity is also low, flag explicitly — content is clean but hollow.

### Step 4 — Structured review report

MANDATORY READ for report structure:
→ [`references/review-report-template.md`](references/review-report-template.md)

### Step 5 — Rewrite

Universal rewrite rules:
1. Never add ideas not in the original; never remove substance
2. Replace every flagged AI phrase with natural language
3. Vary sentence length: mix short punchy lines with longer analytical ones
4. Replace generic openings with a specific hook (story, data point, contrarian claim)
5. Replace summary conclusions with a challenge, principle, or open question
6. Break uniform paragraph rhythm: some short, some long
7. If concrete examples are missing: leave `[ADD SPECIFIC EXAMPLE FROM YOUR EXPERIENCE]` — never invent

For blog, essay, opinion, or personal writing (not encyclopedic, technical, legal, or reference content):
MANDATORY READ → [`references/personality-and-soul.md`](references/personality-and-soul.md) — removing AI patterns produces clean prose; this section is what makes it sound like someone.

MANDATORY READ for channel-specific rewrite rules:
→ [`references/channel-rules.md`](references/channel-rules.md)

Write a draft rewrite, then ask yourself: "What would still make this obviously AI-generated?" List any remaining tells in one line, then produce the final rewrite addressing them. Present only the final rewrite after the review report, not the intermediate draft.

### Step 6 — Self-update

After every review, compare new flags against patterns already in the skill. For each novel pattern:
1. Is it specific enough to illustrate with a concrete example? If not, skip it.
2. Is it universal or channel-specific? Add to the correct reference file.
3. Do not duplicate existing rules.

To add a pattern: attempt to edit the reference file directly. If editing is not available in this context, output the proposed addition as a fenced code block for the user to paste manually.

Report to user:
```
## Skill Update
- [X] new pattern(s) added: [list each + reference file, or "⚠ paste manually — file editing unavailable"]
- [ ] no new patterns found this review
```

### Tuning

Common adjustments after a first review:

| Problem | Fix |
|---------|-----|
| Wrong channel detected | Re-run Step 0; state the correct channel; reload only that channel's rules |
| Rewrite changed ideas | Revert substance changes; keep only delivery edits from Step 5 rules |
| Scores feel off | Ask which dimension feels wrong; re-read only that dimension in `channel-rules.md` and recalibrate |
| Voice profile too generic | Request a more representative sample; re-run Voice Calibration before rewriting |

---

## NEVER

- **NEVER optimize for "sounding human" or "beating detectors"**
  **Instead:** Write for the actual context — medium, audience, reader need.
  **Why:** Both goals produce worse writing. Good context fit reads as human as a side effect.

- **NEVER invent specificity to avoid sounding generic**
  **Instead:** Use fewer verified facts rather than many guessed ones; leave `[VERIFY]` placeholders.
  **Why:** Specificity theater (invented milestones, synthetic quotes, suspiciously exact claims) fails fact-checks and breaks trust faster than vagueness.

- **NEVER inject slang, forced asides, typos, or artificial sentence-length targets to break regularity**
  **Instead:** Natural variety comes from the relationship between thoughts, not from alternating lengths by formula.
  **Why:** Programmatic variation is as recognizable as programmatic regularity.

- **NEVER remove needed headings, lists, descriptive links, or caveats to "sound less AI-written"**
  **Instead:** Preserve accessibility and usability; make text less structured only when the medium genuinely calls for it.
  **Why:** Removing structure to pass a vibe check makes text less useful, not more human.

- **NEVER run long-form diagnostics before required checks**
  **Instead:** Run `references/required-checks.md` first; escalate to diagnostics only when checks pass but the piece still feels off.
  **Why:** Running diagnostics on a draft that hasn't passed required checks produces false positives — diagnostics are calibrated to identify structural problems, not surface-level errors. Running them first treats symptoms as disease.

- **NEVER add ideas to a rewrite that weren't in the original**
  **Instead:** Preserve every argument; change only the delivery.
  **Why:** The user owns the ideas; the skill owns the execution.

- **NEVER apply channel-specific rules from the wrong channel**
  **Instead:** Load only the section for the detected channel in `ai-patterns-channels.md`.
  **Why:** social media hooks, email structure, and IM brevity rules conflict — wrong-channel rules corrupt the rewrite.

- **NEVER match voice from a sample written in a different register than the target content**
  **Instead:** Before applying a voice profile, verify the sample's register (blog, casual, technical) matches the output medium.
  **Why:** A casual social media voice applied to formal documentation produces a register mismatch that undermines both the content and the author's credibility.
