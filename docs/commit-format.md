# Commit format

The default commit format for `hey-mori` repositories. A repository with its
own `docs/commit-format.md` and `scripts/validate-commit-message.sh` follows
those; they implement the same rules.

## Shape

```
<type>: <imperative lower-case summary>

- <what changed, or why>
- <what changed, or why>
```

## Subject

- `type` is one of `feat`, `fix`, `perf`, `refactor`, `test`, `docs`, `chore`.
  `perf` is for speed or resource use; `refactor` must not change behaviour.
- No scope: `fix: ...`, never `fix(ledger): ...`.
- English, imperative, starting lower-case, no trailing period.
- Under about 70 characters; 72 is the hard limit.
- No phase or milestone labels such as `(P2)` or `[M1]`. The branch and the
  issue carry those.

## Body

- One blank line after the subject, then a bullet list only. Every line starts
  with `- `, with no blank lines between bullets and no prose paragraphs.
- Each bullet is one checkable claim about what changed or why. Three to seven
  is typical.
- A trivial change, such as a typo or a broken link, may be subject-only.

## Never include

Emoji, a footer naming the tool that produced the change, `Co-Authored-By:`
lines, "Generated with" lines, pasted validation logs, or filler. Attribution
is the commit author.

## Written by git

These keep the shape git or GitHub gives them:

- Merge commits: `Merge pull request #N from ...`, `Merge branch '...' into ...`.
- Reverts made by `git revert`: `Revert "<subject>"`, a blank line, then
  `This reverts commit <sha>.`, optionally followed by a bullet list.

## Example

```
fix: keep the empty ledger message after a failed reload

- Show the empty state only when the reload succeeded with no records
- Keep the previous rows on screen when the reload fails
- Add a test for a failed reload after a successful one
```
