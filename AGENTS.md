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

## Releasing

Releases are cut by the **Release** workflow (`.github/workflows/release.yml`), never by hand. It is a manual `workflow_dispatch` with one input, `tag`, and it releases the commit at the tip of the branch it is run on. Run it on `main`.

The workflow, in order:
1. Rejects a tag that is not `vX.Y.Z`, or that already exists.
2. Fails unless `version` in `.claude-plugin/plugin.json` and `plugins[0].version` in `.claude-plugin/marketplace.json` both equal `X.Y.Z`.
3. Takes the `## [X.Y.Z]` block from `CHANGELOG.md` as the release notes, and fails if there is none.
4. Creates the tag at the checked-out commit and publishes the GitHub release with those notes.

Nothing is created until every check passes, so a failed run leaves nothing to clean up.

To prepare a release, in one PR:
- Set the same new version in `.claude-plugin/plugin.json` and `.claude-plugin/marketplace.json`.
- Add a `## [X.Y.Z] - YYYY-MM-DD` block at the top of `CHANGELOG.md`, and its `[X.Y.Z]: …` link reference at the bottom.
- Merge to `main`.

Then run the workflow on `main` with `tag=vX.Y.Z`, from the Actions tab (**Release → Run workflow**) or from a shell:

```sh
gh workflow run release.yml --ref main -f tag=vX.Y.Z
```

Afterwards, confirm the release exists and its notes match the changelog block.

NEVER:
- Never push a tag or create a release outside the workflow. A hand-made tag makes the workflow refuse that version, and a hand-written release skips the changelog and version checks.
- Never work around a failed run by hand-writing notes or skipping a check. Fix the changelog or the manifests, merge, and re-run.
