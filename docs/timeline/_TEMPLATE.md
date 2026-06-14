---
date: YYYY-MM-DD
title: "Short, user-facing title for this release"
version: v0.x.0
---

# v0.x.0 — Short, user-facing title

<!--
  This file is a template. To publish a new timeline post:

  1. Copy this file to docs/timeline/YYYY-MM-DD-vX-Y-Z-short-slug.md
     (use today's date and a slug derived from the version, e.g.
     2026-08-15-v0.2.0-real-time-preview.md).
  2. Fill in the frontmatter (date, title, version).
  3. Fill in the sections below. Delete sections that don't apply to
     this release.
  4. Open a PR. The "Timeline post → release" GitHub Action
     (see .github/workflows/timeline-release.yml) will detect the
     new file in docs/timeline/ and create a draft release tagged
     vX.Y.Z whose notes are this file. Review the draft, edit if
     needed, then publish.

  Convention: each release is exactly one new file. Don't edit
  older timeline posts — they're a historical record.
-->

## What changed for users

The first paragraph is the headline. Imagine a user skimming the
release and only reading this. What's the *one* thing they should
take away?

Then list the user-facing changes:

- **Feature name 1** — one sentence on what it does, in the voice
  you'd use in an in-product tooltip.
- **Feature name 2** — one sentence.
- **Bug fix** — "Fixed an issue where X would happen when Y." No
  internal jargon.

## What changed for mentors / admins

Skip this section if the release is user-only. Otherwise, the
same format as above.

## What changed under the hood

Skip this section if it's empty. Use it for:
- New dependencies, new config flags, new environment variables
- Database migrations or schema changes (with a link to the
  relevant Convex migration)
- Anything a developer extending the codebase needs to know

## What's closed

A short list of the issues and Discussions closed by this release,
linked. Format: `- [#N — Title](https://github.com/ZhyJenae/zhyjen-updates/issues/N)`
or `- [Discussion — Title](https://github.com/ZhyJenae/zhyjen-updates/discussions/N)`.

## What's next

Two or three sentences on what the next release is likely to focus on.
These are *commitments of attention*, not *commitments of delivery*
— the team is allowed to change its mind based on what the community
asks for in **Ideas** and **Polls**.

## Try it

If the release is end-user-facing, point at how to see it. Usually
that's just "go to https://zhyjen.app".

If the release is developer-facing (a new env var, a new schema),
paste the `vp install && vp exec convex dev && vp dev` snippet so a
new contributor can exercise it.
