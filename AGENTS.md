# AGENTS.md

## Mission

This repo publishes the `prose` skill for others to install. There is no build; the deliverable is the contents of `skills/prose/`.

The scanner has a test suite. After any change to `scripts/slop-scan.py`, run it from `skills/prose/`:

```bash
python3 tests/run-tests.py
```

`tests/fixtures/clean-blog.md` and the lower half of `tests/fixtures/noun-stack.md` are ordinary prose that must stay silent. If a rule change makes those cases fail, the rule is wrong — do not update the golden to match. Regenerate goldens with `--update` only when you intended the behaviour change.

## Judgment boundaries

ASK:

- Don't let the skill's content drift toward being specific to any one project; it needs to read as generic writing guidance. Ask before changing the license or copyright holder.
