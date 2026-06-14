# GitHub Project setup — one-time manual runbook

This is the one bit of project-hub setup I couldn't do from the CLI
because the `gh` token doesn't carry the `project` scope, and re-auth
requires an interactive browser. It's a 90-second action — three
screens, copy-paste from this file.

## 1. Create the project

Open <https://github.com/orgs/ZhyJenae/projects/new> and fill in:

- **Project name:** `ZhyJen Public Roadmap`
- **Template:** `Team planning` (or `Roadmap` if you see one)
- **Visibility:** ✅ Public
- **Click "Create"**

## 2. Link the repo

In the new project, click **Settings** (gear icon) → **Managed access** →
add the `ZhyJenae/zhyjen-updates` repo as a linked repository. This
makes issues and Discussions from that repo available to add to the
project.

## 3. Replace the readme

Project → **Settings** → **README** → paste the following, replacing
whatever the template inserted:

```markdown
# ZhyJen Public Roadmap

This is the user-facing roadmap for ZhyJen. It surfaces what's
shipping next, what's in flight, and what the team is researching.
Each item below is a real ZhyJen issue or discussion. The
**Status** column tells you where it is. The **Priority** column is
the team's best guess at delivery order — it can change as the team
learns more.

## How to use this board

- **Voting.** Every item has an upvote. The team converts the most
  upvoted items into release milestones.
- **Suggesting.** If a feature isn't here, drop it in
  [Discussions → Ideas](https://github.com/ZhyJenae/zhyjen-updates/discussions/categories/ideas)
  and a maintainer will add it to this board.
- **Status legend:**
  - **Backlog** — not started; waiting on prioritisation.
  - **Next up** — scheduled; will land in the next minor release.
  - **In progress** — actively being built.
  - **Shipped** — done. The release notes will link the relevant commits.
  - **Considering** — on the team's radar but not committed.
  - **Won't do** — explicitly out of scope (e.g. paid tiers, anything
    that conflicts with the project's "free forever" principle).

## How the team decides

See the [project README](https://github.com/ZhyJenae/zhyjen-updates#project-principles)
for the principles. Anything that violates "free forever", "content
first", or "the dashboard is the welcome" is a hard no.

## Cross-references

- [Releases](https://github.com/ZhyJenae/zhyjen-updates/releases) — the user-facing changelog.
- [Timeline](https://github.com/ZhyJenae/zhyjen-updates/tree/main/docs/timeline) — dated project update posts.
- [Discussions](https://github.com/ZhyJenae/zhyjen-updates/discussions) — Q&A, Ideas, Polls, Show and tell, Announcements, General.
```

## 4. Set up the Status field

Project → **+ New field** (in the field strip near the top):

- **Field name:** `Status`
- **Field type:** `Single select`
- **Options (create one for each, in this order):**
  - `Backlog` — color `#BFD4F2` (cool grey-blue)
  - `Next up` — color `#FBCA04` (yellow)
  - `In progress` — color `#0E8A16` (green)
  - `Shipped` — color `#7057FF` (purple)
  - `Considering` — color `#D93F0B` (orange)
  - `Won't do` — color `#EEEEEE` (light grey)

## 5. Add the Priority field

Project → **+ New field**:

- **Field name:** `Priority`
- **Field type:** `Single select`
- **Options:**
  - `P0 — next release`
  - `P1 — this quarter`
  - `P2 — considering`
  - `P3 — backlog`

## 6. Add the starter items

The next milestone candidates from the v0.1.0 timeline post.
Project → **+ Add item** → "Add item from a repository" → search
`ZhyJenae/zhyjen-updates` (or paste URLs). For each, fill in the
**Status** and **Priority** fields. Use the verbatim titles so
people can find them again:

| Title | Status | Priority | Source |
|---|---|---|---|
| Real-time preview on the activity workspace (Monaco → iframe with hot-reload) | Backlog | P1 | the v0.1.0 timeline post, "What's next" section |
| A "challenges" mode for completed activities (stretch goals with their own starter files) | Backlog | P2 | same |
| Mentor-side feedback (short text comments a mentor can leave on a student's `activityProgress.notes`) | Backlog | P1 | same |
| Live site at `zhyjen.app` with the new flow wired up | Next up | P0 | same |
| First pinned welcome post in Announcements (web UI only — the `pinDiscussion` GraphQL mutation doesn't exist) | Backlog | P3 | from the post-rollout notes |

## 7. Set up the views

Project → **+ New view** → **Board** → name it `By status`. This is
the default view you'll use day-to-day.

Add a second view: **+ New view** → **Roadmap** → name it
`By priority`. This is the timeline view; great for the
"What's shipping next" conversation in the README.

## 8. Pin the board on the org profile (optional)

Open <https://github.com/orgs/ZhyJenae> → **Projects** tab → pin
`ZhyJen Public Roadmap` so it appears at the top of the org's
Projects list.

---

That's it. The board is now discoverable from the org's profile,
populated with the next-milestone candidates, and wired up to the
issues and Discussions in `ZhyJenae/zhyjen-updates`.
