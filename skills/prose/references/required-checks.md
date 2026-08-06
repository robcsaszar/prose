# Required Checks

For pieces up to ~150 words or three short paragraphs, run checks 1–5, 7, 10, 11, and 12.
For longer pieces, run all checks.

These are tripwires, not goals. Do not output the audit unless asked.

---

1. **Register fit.** Does the format, punctuation, and level of structure match the medium and the user's request? For web, docs, or UI text: did you preserve scannability and accessibility instead of flattening the piece for style reasons?

2. **Concrete-anchor audit.** For each substantial paragraph, point to one concrete anchor. In criticism, reportage, reviews, and analysis: at least one paragraph in the whole piece should be built around a single concrete example or observed consequence rather than category summary. If you cannot point to that paragraph, add one.

3. **Fact discipline.** Pick the three most fragile factual claims in the piece: dates, milestone names, quotes, close paraphrases, public metrics, future claims, causal trend claims, feature labels, motives, hidden system explanations, or claims sourced to vague authorities. If you cannot vouch for them, attribute them, soften them, or cut them.

4. **Source-fit check.** For factual writing, check every exact quote, close paraphrase, public metric, planned event, and causal claim. Do not keep "X caused Y", "X drove Y", or "X proved Y" unless the source supports the relationship. Use weaker relationship language only when that weaker claim is still accurate.

5. **Regularity and sentence-continuity tripwire.** Name the single most repeated visible pattern in the piece. If the same move appears 3 or more times, or dominates two consecutive paragraphs, rewrite at least one occurrence. Also scan for false crispness: two or more neighboring short sentences whose thoughts are tightly related but split apart. If a comma, conjunction, subordinate clause, colon, or semicolon would express the relationship more naturally, combine one pair. If the period creates useful emphasis or clarity, keep it.

6. **Repeated-frame check.** If a central metaphor, contrast, or wording family appears throughout the piece, decide whether it is a useful motif or a too-neat scaffold. Keep it only where it adds force; vary or cut the rest.

7. **Stance and voice.** If the genre expects a visible writer or evaluative stance, state the writer's view in one sentence to yourself. If you cannot, add stance where it does real work. If the genre expects neutrality, did you keep it neutral?

8. **Developed thought.** For any piece longer than four paragraphs, identify one place where the prose pauses, doubles back, or notices a concrete detail off the main line. If the piece runs in a perfectly straight line from claim to conclusion, check whether one example or noticed detail would make it less pre-solved.

9. **Shape and spine.** For any piece longer than three paragraphs, state the organizing principle in five words or fewer and the controlling claim in one sentence. If the shape is basically "starting state → changes → verdict", if paragraphs map one-to-one with named milestones, or if each paragraph is just one labeled topic bucket, restructure.

10. **Over-correction.** Did you add fake-human moves — typos, slang, forced asides, random fragments, or artificial sentence-length targets — just to break a pattern? Then check the conventions you may have changed without being asked: spelling variety (en-GB vs en-US), date format, number format, and quotation-mark style. If the source held one of these consistently, it is a deliberate choice and it stays. Silently Americanising a British writer is an unrequested edit, not a fix. Where the source was inconsistent, pick the variety its audience expects and say which you picked.

11. **Claim typing and invented norms.** Every substantive claim is one of four types — know which one you are writing: (a) *from the data* — present in the source or supplied by the user; state it plainly, no insurance; (b) *computed on an assumption* — true only if the assumption holds; name the assumption in the same breath; (c) *judgment* — your assessment; mark it as one and give the basis, or cut it; (d) *a gap* — needed for the conclusion but missing; name it once, without drama. Then scan for invented norms: no "healthy", "strong", "well within range", "realistic" without a named baseline (a plan, a prior period, a cost floor, an industry benchmark). If you catch yourself writing "as long as churn stays under 3%, the model holds", stop and ask where the number came from.

12. **Verbatim integrity.** List every fixed string in the piece — code, commands, flags, file paths, identifiers, product names, error text, quoted material, legal phrasing, defined terms — and confirm each one is unchanged from the source. A rewrite that improves the prose around a command and edits the command has broken the document. If one had to change, say so in your response rather than leaving the reader to find it.

13. **Hedge economy and punch budget.** Insure a fragile point once — "this looks like", "still a hypothesis" — at the exact claim it applies to; a qualifier after every sentence is its own AI pattern. Then the inverse: count the aphoristic paragraph-closing one-liners. More than one, demote the rest to plain statements. Confirm there is slack somewhere — at least one sentence that isn't trying to impress — and that confidence varies across the text. Every-sentence-lands and every-claim-equally-sure are both machine signatures.

---

**Deterministic pass (when a shell is available).** The mechanical layer is scriptable:

```bash
python3 scripts/slop-scan.py --channel <medium> draft.md
```

Debris hits get fixed unconditionally. Phrase and typography hits are places to look — verify each against the false-positive rules in `ai-patterns-universal.md` before rewriting; an active voice profile or medium convention may allow some (suppress those with `--allow <rule-id>`). No shell: scan `formula-watchlist.md` manually instead.
