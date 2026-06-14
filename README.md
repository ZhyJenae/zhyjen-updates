# ZhyJen — learn to code, build with purpose

> ZhyJen is a free, beginner-friendly coding platform for young creators.
> It teaches real code through short, focused activities with instant
> feedback, a warm curriculum, and a community that cares about purpose
> and character as much as pixels.

This repository is the **public project hub**: announcements, the
roadmap, community discussion, and the user-facing changelog. The
application source code lives at **[ZhyJenae/zhyjen](https://github.com/ZhyJenae/zhyjen)**
(private — ZhyJen is built by a small team and we keep the dev repo
internal while we work out the v0.x shape).

---

## Where to go

| You want to… | Go to |
|---|---|
| Try the app | **[zhyjen.app](https://zhyjen.app)** |
| Read what's new | **[Releases](../../releases)** or [`docs/timeline/`](./docs/timeline/) |
| Suggest a feature or vote on what ships next | **[Discussions → Roadmap](../../discussions/categories/roadmap)** |
| Ask "how do I…" or get help | **[Discussions → Q&A](../../discussions/categories/q-a)** |
| Share what you built | **[Discussions → Show and tell](../../discussions/categories/show-and-tell)** |
| Report a student-facing bug | **[New issue](../../issues/new/choose)** |
| Read the code or contribute | **[ZhyJenae/zhyjen](https://github.com/ZhyJenae/zhyjen)** (private — request access) |

---

## Current state — v0.1.0 (Student-First Experience)

The v0.1 milestone ships the full student-first experience end-to-end.
A brand-new student can sign up, answer one placement question, and
land on a curated Start-here view with the first three activities of
the right Track for their experience level.

What's in this release:
- **4-step onboarding** with a single placement question ("Have you
  written any code before?") that seeds the student's starting Track.
- **Start-here dashboard** that renders the first three activities of
  the student's current Track in `order`, with a pinned "Start" CTA on
  the first. The moment the student opens any Activity, the regular
  dashboard takes over on their next visit.
- **Track-filtered activities list** at `/activities`, with one
  segmented-control tab per Track (plus "All"). Locked Tracks are
  visible but greyed, with a tooltip explaining the unlock condition.
- **Invitation accept flow** at `/invitations/:token` — mentors can
  invite students via a shareable link. The page handles Clerk
  sign-in, the placement question (if the student hasn't answered it
  yet), and a single "Join workspace" button that creates the
  membership and routes to the dashboard.
- **Mentor view** at `/mentor` showing one row per student with their
  current Track, last activity, status, and last-updated date.
- **Progress strip + advance-unlock toast** on the regular dashboard.
  A slim pill at the top while the student is on their starting Track
  reads "You're on **{Track}** — X of Y activities completed". A
  one-time toast fires the first time they unlock a new Track.

What's next: see the **Roadmap** discussion for the candidates.

---

## Project principles

These are the values the team holds when trade-offs come up. They
aren't aspirational — they're how decisions actually get made.

1. **Content first.** A small, complete activity library beats a big,
   half-finished one. We ship six activities before we ship sixty.
2. **One question, not a test.** The placement question is for *the
   student*, not for the platform. We never score it. We never
   "level-test" the user.
3. **Free forever.** No paywalls, no premium tiers, no "Pro" badge.
   ZhyJen is free for the same reason a public library is free.
4. **Faith-informed, not preachy.** The connection between coding and
   character is real and personal. We surface it gently (reflection
   prompts) rather than lecturing.
5. **The dashboard is the welcome.** A brand-new student lands on a
   Start-here view, not a feature tour. We optimise for the first
   five minutes, not the first five features.

---

## How to follow along

- **Watch this repo** (click "Watch" → "All Activity") to get notified
  of every release and every Announcement discussion.
- **Subscribe to Releases only** if you want the user-facing changelog
  without the discussion noise.
- **Star the repo** if ZhyJen is useful to you — it helps others find
  the project.

---

## Maintainers

ZhyJen is built by [@titan-65](https://github.com/titan-65) and
contributors. The application source is at
**[ZhyJenae/zhyjen](https://github.com/ZhyJenae/zhyjen)**.
