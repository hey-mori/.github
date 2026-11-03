# Contributing to Mori

This guide applies to every repository in the `hey-mori` organization that does
not have a `CONTRIBUTING.md` of its own. It holds what all Mori repositories
share.

Found a vulnerability? Do not open an issue. Follow
[SECURITY.md](SECURITY.md).

## Organization rules and repository rules

This file sets the common ground: how work is proposed, branched, verified and
merged, and how commits and pull requests are written.

Each repository documents what only it can know: its verification gate and how
to run it, its toolchain, platform testing, release steps, and any stricter
rule. Look in the repository for, in this order:

1. `CONTRIBUTING.md`
2. `CLAUDE.md` or another agent guide
3. `docs/git-workflow.md` and `docs/commit-format.md`

Where a repository's documents and this file disagree, the repository wins.

## How a change lands

1. **Check what is in flight.** Run `git fetch --prune`, then read the open
   pull requests and issues. If someone is already working on the same problem
   or the same area, continue that work instead of starting a second branch.
2. **Open an issue first** when the change needs a decision or a durable
   record. A small, clearly scoped fix can go straight to a pull request.
3. **Branch from an up-to-date `main`** as `<type>/<area>-<slug>`, for example
   `fix/ledger-empty-state`. `<type>` is the commit type of the main change.
   Keep the branch short-lived; one that cannot merge within a few days is
   usually two changes.
4. **Commit in small, self-contained steps** that follow the
   [commit format](docs/commit-format.md). If the repository has
   `scripts/setup-git-hooks.sh`, run it once per clone so a malformed message
   is rejected before the commit exists.
5. **Verify locally** with the repository's documented gate. CI runs on the
   pull request too, but the local result is the evidence the pull request
   reports.
6. **Open a pull request.** Title it like a commit subject. In the body, say
   what changed and why, which checks actually ran and their result, and what
   was not verified.
7. **Merge with a merge commit, then delete the branch.**

## Licence and sign-off

Each product repository is licensed under the
[Mozilla Public License 2.0](https://www.mozilla.org/MPL/2.0/) (`MPL-2.0`). Its
own `LICENSE` file is the licence, and its README names the copyright holder.
A contribution is accepted under that same licence. There is no separate
contributor agreement and no transfer of copyright: you keep the copyright in
what you wrote.

Every commit in a pull request from outside the organization carries a
sign-off, as the last block of the message after a blank line:

```
Signed-off-by: Your Name <you@example.com>
```

`git commit -s` adds it from your `user.name` and `user.email`, which must
match the commit's author. By signing off you certify the
[Developer Certificate of Origin 1.1](https://developercertificate.org): that
you wrote the change, or otherwise have the right to submit it under the
repository's licence. A `dco` check on the pull request names any commit
without one, and `git rebase --signoff main` adds it to every commit on a
branch. Maintainers' own commits do not need it.

- **Code you did not write yourself**, generated code included, is yours to
  account for. Do not submit it unless its origin allows you to license it
  under MPL-2.0.
- **Third-party code** keeps its own licence and notice. Add it only under a
  licence compatible with MPL-2.0, and say so in the pull request.
- **Names and logos.** The licence grants no rights to the Mori names or logos
  as trademarks (MPL-2.0 §2.3). A modified version you distribute may say it
  is based on Mori, but must not use the Mori name or logo as its own name or
  icon.

## Rules for `main`

- Nothing is committed directly to `main`. Every change arrives through a pull
  request.
- `main` is never rewritten, and a branch that someone else may have pulled is
  never force-pushed.
- Pull requests merge with a merge commit (`--no-ff`), not a squash or a
  rebase. Each commit is already a reviewed record, and notes and issues cite
  commits by SHA, so the SHAs must survive the merge.
- Hooks are not skipped. Do not use `--no-verify`.

## Agree before you build

Some changes alter what a product promises rather than how it keeps the
promise. Discuss them in an issue and get agreement before writing code:

- what Mori reads, stores, keeps, or sends anywhere
- privacy, retention and deletion behaviour
- storage formats, schemas and migrations
- the boundary between products
- releases, signing and distribution

Bug fixes, tests, refactoring within an agreed design, and documentation that
has fallen out of date do not need this step.

## Writing

- Commits, branch names, code comments and developer documentation are in
  English.
- Product UI copy is Korean-first unless the repository says otherwise.
- Do not use the em dash (U+2014) anywhere: not in copy, code, comments or
  commits. Use a comma, a middle dot (`·`) or two sentences. An en dash in a
  numeric range such as `3–7` is fine.
