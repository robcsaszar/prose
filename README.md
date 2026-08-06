<p align="center"><img src=".github/prose.png" width="400" alt="prose banner"/></p>

# prose

Writing skill drafts & humanizes text. Kills AI patterns, matches your voice.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![skills.sh](https://skills.sh/b/robcsaszar/prose)](https://skills.sh/robcsaszar/prose)

A drafting and review skill for prose: writes new content in the correct voice and structure for the medium, or scans existing text for AI writing patterns and rewrites it in an authentic human voice.

This skill follows the [Agent Skills specification](https://agentskills.io/specification) so it can be used by any skills-compatible agent.

## Installation

### npx skills
    npx skills add robcsaszar/prose

### Marketplace
    /plugin marketplace add robcsaszar/prose
    /plugin install robcsaszar-prose@prose

### Manually
Copy the `skills/prose/` directory into your project's `.claude/skills/`.

## What it does

The skill runs in two modes, detected from context. Draft mode takes a topic, brief, or outline and produces new content, first asking what the reader needs to do or feel, what would surprise them, and what concrete example can carry the piece, then drafting and running required checks. Review mode takes existing text, auto-detects its channel (blog, social media, email, IM, documentation, or creative), scans it against a library of universal and channel-specific AI writing markers, scores it, and produces a rewrite that keeps every original idea while replacing flagged phrasing and restoring a human voice.

Channels are not cosmetic. A runbook is scored on whether a reader can complete the task, not on whether it sounds like a specific person, and the structural uniformity that would be a tell in a blog post is the target in a procedure. Fiction and poetry keep the em dashes that mark interrupted speech. Applying blog rules to either is the failure the channel split exists to prevent.

It supports voice calibration from a writing sample so drafts and rewrites can match a specific person's sentence rhythm, word choice, and structural habits, and it updates its own pattern library with novel AI-writing markers found during review.

Anti-slop enforcement runs on three mechanisms rather than vibes. A deterministic scanner (`scripts/slop-scan.py`) catches mechanical tells — chat debris, formula phrases, typography artifacts, structural monotony metrics — with stable, repeatable output, and runs on both new drafts and reviewed text. Every flag then faces adversarial verification: the skill argues each one is a false positive before it may enter the report, so legitimate prose is protected from over-editing. Rewrites go through an elimination loop — rewrite, re-scan, then prosecute the result as if it were still AI-generated — until the text survives both the script and the argument, including the second-order tells that surface-level cleanups leave behind (uniform confidence, an aphoristic close on every paragraph, template document shapes). Voice calibration can persist to a profile file that future sessions reuse, and the profile feeds the scanner's allowlist so personal style is never flagged as slop.

The scanner's rules are covered by a golden-file test suite (`python3 tests/run-tests.py`, no dependencies). Most of its cases assert silence rather than detection: a clean-prose fixture fails the suite if a rule change starts flagging ordinary writing, which is the failure mode that matters for a tool whose job is to leave good text alone.

## License
[MIT](LICENSE) © Rob Csaszar
