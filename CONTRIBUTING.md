# Contributing to Mori

This is the default guide for `hey-mori` repositories that have no
`CONTRIBUTING.md` of their own. Where a repository documents its own workflow
(`CONTRIBUTING.md`, `CLAUDE.md`, `docs/git-workflow.md`), that document wins.

## Start from the current state

1. Fetch and prune, then read the open pull requests and issues. If the same
   problem or the same area is already in progress, continue that work instead
   of opening a second branch.
2. Open an issue first when the change needs a decision or a durable record.
   A small, clearly scoped fix can go straight to a pull request.

## Branch, pull request, merge

- Branch from an up-to-date `main` as `<type>/<area>-<slug>`, for example
  `fix/ledger-empty-state`. `<type>` is the commit type of the main change.
- Keep branches short-lived. A branch that cannot merge within a few days is
  usually two changes.
- Nothing is committed straight to `main`, and `main` is never rewritten.
  Never force-push a branch someone else may have pulled.
- Title the pull request like a commit subject.
- Merge with a merge commit (`--no-ff`). Do not squash or rebase-merge: each
  commit is already a well-formed record, and notes and issues cite commits by
  SHA.
- Delete the branch once it has merged.

## Commits

Follow [the commit format](docs/commit-format.md) unless the repository defines
its own. Where a repository ships `scripts/setup-git-hooks.sh`, run it once per
clone so a malformed message is rejected before the commit exists. Never skip
the hooks with `--no-verify`.

## Verification

Run the repository's documented local gate before opening a pull request and
again before merging. Remote CI may be manual-only, so the local result is the
evidence.

In the pull request, list only the checks that actually ran, with their result.
Say what was not verified, such as a platform you could not run, instead of
leaving it out.

## Language and writing

- Repository artifacts are English: commits, branch names, code comments and
  developer documentation.
- Product UI copy is Korean-first unless the repository says otherwise.
- Never use the em dash (U+2014): not in copy, code, comments or commits. Use a
  comma, a middle dot (`·`) or two sentences. An en dash in a numeric range
  such as `3–7` is fine.

## Security

Never put vulnerability details in an issue or a pull request. Follow
[SECURITY.md](SECURITY.md).
