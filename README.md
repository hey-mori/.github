# hey-mori/.github

The organization's shared policy repository. It holds what every Mori
repository has in common: how to contribute, how commits and pull requests are
written, how to report a vulnerability, and the public organization profile.

Product code, release tooling, CI and operational detail live in the
repositories that own them, not here.

## Contents

| Path | GitHub uses it as |
| --- | --- |
| `CONTRIBUTING.md` | contributing guidelines |
| `SECURITY.md` | security policy |
| `.github/PULL_REQUEST_TEMPLATE.md` | pull request template |
| `.github/VULNERABILITY_REPORT.yml` | private vulnerability report form |
| `profile/README.md` | the public profile at [github.com/hey-mori](https://github.com/hey-mori) |
| `docs/commit-format.md` | nothing by itself; linked from `CONTRIBUTING.md` |

## How GitHub applies these files

- GitHub reads defaults only from a **public** repository named `.github`.
- A default is used by **every** repository in the organization, public or
  private, that does not have its own file of that type.
- A repository's own file wins, entirely. GitHub looks in the repository's
  `.github/` folder, then its root, then `docs/`, and only falls back to this
  repository if none of them has the file. Nothing is merged.
- Defaults are not copied into other repositories. They do not appear in their
  clones or history, and a change here applies everywhere at once.
- The report form applies only where private vulnerability reporting is turned
  on, which GitHub allows on public repositories only.
- Licenses cannot be defaults. Each repository carries its own.

To see what a repository actually uses, open its **Insights → Community** page
(public repositories) or check whether it has its own copy of the file.

## What is not here, on purpose

- **Issue templates.** GitHub treats a repository's whole `ISSUE_TEMPLATE`
  folder as one unit, so a central set reaches only repositories with none of
  their own. Each repository keeps its own templates.
- **A code of conduct and a support guide.** Add them when the first
  repository opens to outside contributors.
- **A members-only profile.** That lives in a private `.github-private`
  repository, if one is ever needed.

## Maintaining this repository

- **Everything here is public.** Leave out private repository names, internal
  design, hostnames, runner and deployment details, release plans, local
  paths, and anything taken from a private repository's issues or pull
  requests.
- **Keep only what every repository shares.** A verification command, a merge
  script or a toolchain version belongs to the repository that runs it.
- **Change it like code.** Use a branch and a pull request, merge with a merge
  commit, and keep each default in its own commit so its reach can be
  reviewed on its own.
- **Use absolute links in the pull request template and the report form.**
  GitHub shows them inside other repositories, where a relative link would
  resolve against that repository. Other files may link relatively.
- **Keep the policy true.** When a repository adds its own policy, or a
  product becomes public, update what this repository says about it.

## History

The Mori repositories moved here from the `swarea` organization. The defaults
in `swarea/.github` no longer apply to them. Documents there that Mori still
links to, such as the repository mark rule, stay where they are and are not
copied here.
