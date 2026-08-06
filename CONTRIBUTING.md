# Contributing

Thanks for considering a contribution to `prose`. This is a small, single-skill repo.

## Before you start

- **False positive or false negative in the AI-pattern detection?** Open an issue with the exact text flagged (or missed) and which reference file's rule it maps to. This is the highest-value kind of report here.
- **Proposing an addition to the reference material?** Open an issue with the pattern, whether it's universal or channel-specific, and a concrete example. See `skills/prose/SKILL.md`'s Step 6 for the same criteria the skill applies to itself: specific enough to illustrate, correctly scoped, and not a duplicate of an existing rule.
- **License or copyright holder:** don't change without asking first.

## Making a change

1. Fork and branch from `main`.
2. Keep edits inside `skills/prose/`. Reference files are split by concern (universal patterns, channel-specific patterns, channel rules, drafting core, and so on); add a new pattern to the file that already owns that concern rather than starting a new one.
3. Note that this skill's own content legitimately uses heavy em-dash and AI-pattern examples as its subject matter. Don't "clean up" prose inside `SKILL.md` or `references/` to remove those. They're the material the skill is built to detect.

## Questions

Open an issue. There's no separate chat or forum for this project.
