# Security policy

This is the default policy for `hey-mori` repositories that have no
`SECURITY.md` of their own. Mori is local-first software that reads what is on
the user's machine, so a report about data leaving the device, or being kept
longer than promised, is in scope even when no code is exploited.

## Report privately

**Do not open a public issue, discussion or pull request for a vulnerability.**

1. Use [Report a vulnerability](https://github.com/hey-mori/.github/security/advisories/new)
   on this repository. It is private end to end, and it works even if you
   cannot see the repository the problem is in.
2. If that form is unavailable, open an
   [issue here](https://github.com/hey-mori/.github/issues/new) that says only
   that you have found something and asks for a private channel. Leave every
   technical detail out of it.

A useful report names the product and version or commit, the steps to
reproduce, and what you saw against what you expected. A proof of concept helps
and is not required.

## What to expect

- An acknowledgement within a week. No response time is guaranteed.
- You will be told whether a fix is planned, and roughly when, before anything
  is published.
- There is no bug bounty.

## Scope

In scope: code in the Mori repositories, the artifacts they publish, and the
builds that produce them.

Out of scope: third-party services and platforms Mori runs on or integrates
with (report those to their owners), social engineering, and anything that
needs access to a maintainer's account.

## Please do not

- Access, change or delete data that is not yours.
- Test against someone else's installation when a local one would do.
- Publish details before a fix is released, or before a decision not to fix has
  been explained to you.
