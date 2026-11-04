# Security policy

This policy applies to every repository in the `hey-mori` organization that
does not have a `SECURITY.md` of its own. A repository with its own policy
follows that one.

## Reporting a vulnerability

**Do not report a vulnerability in a public issue, discussion, pull request or
commit.** Anything posted there is public at once.

Report it privately with the affected repository's own form, under its
*Security* tab:

- Mori: [Report a vulnerability](https://github.com/hey-mori/mori/security/advisories/new)
- Mori Lens: [Report a vulnerability](https://github.com/hey-mori/mori-lens/security/advisories/new)
- Mori Browser Extension: [Report a vulnerability](https://github.com/hey-mori/mori-browser-extension/security/advisories/new)
- Mori Web: [Report a vulnerability](https://github.com/hey-mori/mori-web/security/advisories/new)

If you are not sure which repository is affected, or the problem spans more
than one, use
**[this repository's form](https://github.com/hey-mori/.github/security/advisories/new)**
and name the product and the version.

- You need a GitHub account and must be signed in.
- The report is not public. It reaches the Mori maintainers, and stays private
  until an advisory is published, if one is.

### If the form is not available

Open an [issue in this repository](https://github.com/hey-mori/.github/issues/new)
titled **Security contact request**, with this as the only text:

> I would like to report a security issue privately. How can I reach you?

Do not name the product, component, version or kind of problem. A maintainer
will reply with a private way to send the details.

## What to include

- The product, its version or commit, and the platform.
- Steps to reproduce, and a proof of concept if you have one.
- The impact: what an attacker can do, or what data leaves the device, is kept
  longer than promised, or is read without permission.
- Whether you have told anyone else, and any disclosure date you have in mind.

## What happens next

Mori is maintained by a small team. These are targets, not guarantees.

| Step | Target |
| --- | --- |
| Acknowledge the report | within 7 days |
| Assess it: accepted, more information needed, or not a vulnerability | within 30 days |
| Fix an accepted report | a plan and a date, shared with you, based on severity |

You will hear from us at each step, including when a target slips.

## Disclosure

We follow coordinated disclosure. Please keep the details private until a fix
is released, or until we agree on a date together.

We ask for up to 90 days from acknowledgement to release a fix. If we need
longer, we will explain why and agree a new date with you before it passes.

Once a fix is released, it is disclosed through a GitHub security advisory if
the affected repository is public, or otherwise in the notes of the first
release that contains it.

## Supported versions

Mori has no public release yet. Reports are assessed against the current
development version. This section will list supported versions once releases
exist.

## Scope

In scope:

- Code in `hey-mori` repositories, the artifacts they publish, and the builds
  and release process that produce them.
- Privacy failures. Mori is local-first software, so data leaving the device,
  being kept longer than promised, or being read outside what the user
  connected is in scope even when nothing is exploited in the usual sense.

Out of scope:

- Third-party services and platforms that Mori runs on or integrates with.
  Report those to their owners.
- Attacks that require an attacker who already controls the user's account or
  device.
- Social engineering, and anything that requires access to a maintainer's
  account.

## Recognition

There is no bug bounty and no payment for reports. With your permission, you
will be credited in the advisory or the release notes.

## Testing in good faith

- Test only against your own installation and your own data.
- If you reach data that is not yours, stop, and include that in your report.
- Do not degrade a service or another person's use of Mori.
- Do not publish details before a fix is released or the agreed date passes.
