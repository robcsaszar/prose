# Changelog

All notable changes to this project are documented here. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versioning follows [SemVer](https://semver.org/).

## [0.8.0] - 2026-08-08

### Added

- **Repetition and shape tells.** Four structural patterns the scanner passed clean: anaphora (three or more consecutive sentences opening with the same words), ordinal-labelled paragraphs that are a numbered list in paragraph costume, verbatim duplication of a paragraph or sentence, and countdown negation ("Not a bug. Not a feature. A design flaw."), which every existing parallelism rule missed because they all require a `but` or a comma splice. These are ordered first deliberately: structural habits survive paraphrase and outlast the vocabulary of any one model generation.
- **Staging and assertion tells.** The framing moves that promise significance instead of earning it: manufactured suspense (`Here's the kicker`, `Here's where it gets interesting`), self-posed questions answered on the spot (`The result? Devastating.`), patronizing analogy frames (`Think of it as...`), futurism invitations (`Imagine a world where...`), asserted obviousness (`The truth is simple`, `History is unambiguous`), the dramatic reveal (`the real story is`), grandiose stakes inflation (`will define the next era`), and coined concept labels used as though already defined (`the supervision paradox`). Performative vulnerability joins the second-order tells in Part 5, where it belongs — it is what a cleanup pass produces when told to sound more human.
- **Surface artifact tells.** Magic adverbs, scoped to the adverb-plus-transformation-verb pair (`quietly reshaping`) so that `she answered quietly` and `a deeply nested config` stay silent, and unicode arrows used as decoration in running prose.
- **Judgment-only additions** for the tells no regex should attempt: one-point dilution and fractal summaries get audits in `long-form-diagnostics.md`; historical analogy stacking gets a pattern entry. Automating these would flag ordinary prose more often than slop.
- **Required check 14, staging and assertion.** Counts the moves that promise significance instead of delivering it and budgets them at one per piece. Appended rather than inserted so the existing check numbering, which the short-piece routing depends on, is untouched.
- **Four scanner rule-ids and four structure notes.** New flags `rhetorical-fragment`, `analogy-framing`, `futurism`, `asserted-obvious`, `adverb`, and typography rule `arrows`; new notes `anaphora`, `ordinal-listicle`, `concept-label`, and `duplicate-block`. Existing `hook`, `inflation`, and `parallelism` gained regexes rather than new ids, so hits keep aggregating under the habit they belong to.
- **Five test cases and four fixtures**, including `clean-technical.md`, a second false-positive guard written to brush every new rule without being slop — an ordinary "she answered quietly", a "deeply nested" config, "the first time I have seen", "scope creep", and a real question the text goes on to answer. It asserts silence, so a rule that starts flagging ordinary writing fails the build. `repetition.md` is paired across docs and blog to prove the new channel suppressions are load-bearing in both directions.

### Changed

- `CHANNEL_SUPPRESS` gains entries for the new rules where a medium legitimately breaks them. Documentation suppresses anaphora, ordinal labels, duplicate blocks, and arrows, because procedures enumerate steps, repeat warnings on purpose, open consecutive steps the same way, and write menu paths with arrows. Creative suppresses anaphora, rhetorical fragments, analogy frames, futurism, and concept labels, because anaphora is a device in verse and a character is allowed to talk in stock phrases.
- The invented-concept-label note reports only when two or more distinct coinages share a text, and an allowlist exempts established terms that fit the same shape (`scope creep`, `the liquidity trap`, `the digital divide`, `the sunk cost fallacy`). One such phrase is usually a real term of art; a cluster is the tell.
- `ai-patterns-universal.md` Part 6 gains four false-positive rules: established terms that look like coinages, arrows in notation rather than prose, genuine self-correction as distinct from performative vulnerability, and repetition the medium requires.
- Required checks 5, 6, and 13 absorbed the new tells that belong to tripwires already in place, rather than growing the list. Check 6 gains a concrete threshold for the dead metaphor: one image carrying five or more paragraphs.
- Two whole-text scanner regexes now match across a line break. They used literal spaces, so a wrapped line put a newline in the middle of the phrase and the pattern silently missed it.

### Fixed

- The review report template offered four channels and "Other" although Step 0 has detected six since 0.7.0. A review of a runbook or a scene had nowhere correct to record its own detection.
- `SKILL.md` opened with an H1 of "Writing" while its frontmatter `name` was `prose`, a leftover from the rename in 0.7.0.

## [0.7.0] - 2026-08-06

### Added

- **Documentation channel.** Step 0 now detects procedures, specs, runbooks, and reference pages, and they are scored on Task Completion, Precision, and Consistency instead of Authenticity — nobody needs a runbook to sound like a specific person. Adds documentation markers (difficulty minimisers, hedging in a spec, synonym cycling across a page, steps with no stated result, narrative framing, prerequisites discovered mid-procedure) and rewrite rules covering one action per sentence, condition/action/result steps, positive instructions, consistent terminology, and short noun groups.
- **Creative channel.** Step 0 now detects fiction, poetry, memoir, and scripts. The em-dash prohibition is suspended inside dialogue and verse, where the dash marks interruption and nothing else does that job. Adds creative markers (the explained ending, one register for every character, stock scene openings, every scene resolving, even sensory distribution) and rewrite rules that preserve intentional ambiguity, cadence, and character voice.
- **Deterministic anti-slop scanner** (`scripts/slop-scan.py`): scriptable detection of chat debris, formula phrases, typography artifacts, and structural monotony metrics (sentence-length windows, uniform paragraphs, uniform confidence, aphorism budget), with per-channel modes, a rule allowlist for voice profiles, stable sorted output, and gate-friendly exit codes. Wired into Draft Mode Phase 2, Review Mode Step 1, and `required-checks.md`.
- **Test suite** (`tests/`): a golden-file runner over ten cases with no third-party dependencies. Includes a clean-prose fixture that fails the build if a rule change starts flagging ordinary writing, paired cases proving each channel's suppressions are load-bearing, and a case proving `--allow` cannot silence debris.
- Adversarial verification (Review Mode Step 2): every flag must survive a strongest-case false-positive defense before entering the report; debris is always confirmed, and dismissed counts are reported. Protects legitimate prose from over-editing.
- Elimination loop in the Review Mode rewrite step: rewrite → re-scan → prosecute the result as still-AI, up to three rounds, with explicit exit criteria and justified exceptions.
- Persistent voice profiles: `references/voice-profile-template.md`, saved as `voice-profile.md` after calibration, reused across sessions, feeding the scanner allowlist; incremental "learn from this text too" updates.
- Scanner rules for nominalizations (`perform an analysis of`, `made a determination`) and wordiness (`in order to`, `due to the fact that`, `at this point in time`) — phrases the pattern library already documented but nothing mechanically detected.
- Scanner rule for noun stacks: four or more content words with no preposition to join them, anchored to a determiner and requiring two derived nouns, so ordinary four-word phrases stay silent.
- "Second-Order Tells" part in `ai-patterns-universal.md`: patterns that survive or are produced by a cleanup pass — uniform confidence, no-slack prose, aphorism budget, upgraded parallelisms, balanced antitheses, fragment pairs, verdict verbs, recycled hooks, replacement tics, and the templated document shape.
- Structure-first framing backed by a 2026 structural-detection study (arXiv:2604.03136), with shelf-life warnings on era-dependent AI vocabulary; new structural markers: stating the moral, emotion as body metaphor, the outline test, overgeneralized sourcing.
- Epistemics: four-way claim typing (from data / computed on assumption / judgment / gap), a NEVER rule against invented norms and thresholds, hedge economy, and "editing is not fact-checking".
- Human-writing protections in `ai-patterns-universal.md`: plain copulas and verbs, true superlatives, hedges on real soft spots, direct reader address, slack sentences, visible self-correction.
- `drafting-core.md` rules 17 (use the same term for the same thing) and 18 (preserve what is not prose), plus nominalization and noun-stack examples under rule 5, and a flat-definition rule.
- `required-checks.md` check 12, verbatim integrity: confirm every command, identifier, product name, and quotation is unchanged from the source.
- NEVER rules against applying blog rules to fiction, rewriting fixed strings, and silently converting spelling variety or date format.
- Attribution of the plain-word, cut-the-word, and active-verb rules to Orwell's "Politics and the English Language" (1946).
- Whole-piece correction examples in `examples.md`; new long-form diagnostics (confidence spread, analogy audit, question audit, read-aloud pass).
- Edit-scope modes for Review Mode rewrites (free / careful / minimal).

### Changed

- `CHANNEL_SUPPRESS` in the scanner replaces three hardcoded channel conditionals, so per-channel behaviour is declared in one table. Blog, social, email, and IM output is byte-identical to before; only the docs channel changes, and only to stop reporting the structural uniformity that procedures are supposed to have.
- Universal rewrite rules 3–6 now carry explicit channel exceptions. They told every rewrite to vary sentence length, break paragraph rhythm, and replace summary conclusions, all of which are wrong for documentation and partly wrong for creative work.
- Check 10 (over-correction) now covers spelling variety, date format, and quotation style as conventions a rewrite must not change unasked.
- `ai-patterns-universal.md` Part 6 gains three false-positive rules: fixed strings, craft in the creative channel, and the uniform shape of a procedure.
- Review Mode renumbered to eight steps to accommodate adversarial verification; review report template now carries confirmed-only flags plus a dismissed count.

### Fixed

- `--allow` could suppress DEBRIS hits, contradicting both the scanner's own documentation and the skill's instruction that debris is always confirmed. Debris now ignores channel suppression and `--allow` alike.
- Plugin manifests reported a stale version while the changelog documented a newer one as released. Both manifests now track the changelog.

## [0.5.0] - 2026-07-10

### Added

- Initial release: prose skill.

[0.8.0]: https://github.com/robcsaszar/prose/compare/v0.7.0...v0.8.0
[0.7.0]: https://github.com/robcsaszar/prose/compare/v0.5.0...v0.7.0
[0.5.0]: https://github.com/robcsaszar/prose/releases/tag/v0.5.0
