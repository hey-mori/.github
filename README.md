# hey-mori/.github

Organization-wide defaults for the Mori repositories. GitHub reads this
repository only because it is public and named `.github`; nothing here is
meant to be cloned or built.

## What lives here

| Path | Used by GitHub as | Applies to |
| --- | --- | --- |
| `CONTRIBUTING.md` | contributing guidelines | repositories with no `CONTRIBUTING.md` of their own |
| `SECURITY.md` | security policy | repositories with no `SECURITY.md` of their own |
| `.github/PULL_REQUEST_TEMPLATE.md` | pull request template | repositories with no pull request template of their own |
| `profile/README.md` | organization profile | the public page at github.com/hey-mori |
| `docs/commit-format.md` | nothing (a linked reference) | read through `CONTRIBUTING.md` |

## How the defaults behave

- A repository's own file always wins, and wins entirely. The two are never
  merged, so a repository that adds its own `SECURITY.md` stops seeing this one.
- Defaults are not copied into a repository. They do not appear in a clone, and
  a change here takes effect everywhere at once.
- Issue templates are deliberately absent. GitHub treats the whole
  `ISSUE_TEMPLATE` directory as one file, so a central set would reach only
  repositories that define none, and each Mori repository keeps its own.
- Which repository uses which default changes over time. Check the repository,
  not a list written here.

## Rules for editing

- **Everything here is public.** Do not add private repository names, internal
  design, hostnames, runner or deployment details, release plans, local paths,
  or anything from a private repository's issues.
- **Keep only what every Mori repository shares.** A verification command, a
  merge script or a toolchain version belongs to the repository that owns it.
- **Use absolute links in the pull request template.** GitHub pastes the
  template into another repository, where a relative link would resolve
  against that repository. Other files here may link relatively.
- Change one default per pull request, so its reach can be checked on its own.

## Relationship to swarea/.github

The Mori repositories moved here from the `swarea` organization. The defaults
in `swarea/.github` no longer apply to them. Documents there that Mori still
links to, such as the repository mark rule, stay where they are and are not
copied here.
