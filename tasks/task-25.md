---
id: task-25
uid: 3ac5f91c-c47f-4dc6-ad32-b11b4a107273
type: task
title: "README/media review hub: case-by-case Showcase layouts"
state: "in-progress"
priority: "high"
effort: "medium"
relatedFiles: ["VISION.md", "docs/public-readiness.md"]
accord:
  status: "claimed"
  acceptance: ["One compact Sideshow review hub includes all eight requested repos with summary, status, existing preview link and exact decision", "Theme and verdigris's revised proposals appear first; each layout recommendation follows the case-by-case Showcase guidance", "Owners update through this hub instead of opening parallel review asks; privacy holds remain explicit", "No new captures, render investigation or public changes before approval"]
  claimedAt: "2026-11-17T15:38:11Z"
  updatedAt: "2026-11-17T17:57:06Z"
createdAt: "2026-11-17T15:38:09Z"
updatedAt: "2026-11-17T17:57:06Z"
assignee: "algorant"
---
## Current direction — Algorant, 2026-11-17, via Herdra

"ok generally 'Screenshots' should just be 'Showcase' or, in repos where its not needed, can just be images pasted in a 3 or 4 image row under the banner. should be kind of case by case. that goes for the omarchy-verdigris-theme readme, a well as verdigris readme ... come up with a plan and confirm what I'm saying"

"then, lets consolidate all these major changes into one sideshow display ... make links to each preview or post or merge request, whatever makes the most sense ... having one sideshow thing for each change like this seems inefficient."

One topic session, one compact review post: theme and verdigris revisions first, then nvim, herdra, tandem, pi catalog, algOS placeholder, herdr-agent-tree. Each row has a one-line summary, current status, preview link and exact decision. Existing sessions are supporting previews/history, not parallel review asks.

Owners have been asked for one-line layout recommendations. A bounded text-only helper assembles existing post metadata; no captures, no render investigation, no new assets. No public changes before approval. Showcase or compact 3–4-image row case-by-case; demo first only when useful. Preserve privacy findings/holds and no-live-capture rule; exclude cutover/network work.

## Historical pattern A specification (superseded where rigid)


## Description

Algorant (2026-11-17, via Herdra): "yes for herdra to establish A, the demo sells it first. algOS and some other repos should also follow this pattern, like my pi setup etc. the web-ps would have to be created for some of those, but in algos' case we seem to have removed it"

## The standard (in VISION.md and the readiness map, 05c49c4)

One looping demo right after the intro (animated WebP, q90, about 10–12 s, sped up, full width); stills in a `## Screenshots` section near the end, all the same size, 2-column table, small captions. The zellij / yazi / gitui / Hyprland pattern. A pure colour scheme may need only the stills.

## Per-repo state (READMEs read on GitHub, 2026-11-17)

| Repo | Visibility | Demo | Screenshots section | Owner |
|---|---|---|---|---|
| herdra | private | ✓ `images/shots/tour.webp` (layout A being applied) | in progress | herdra manus |
| pi | public | needs one (likely a headless VHS of pi in a terminal) | none; banner only | .pi Ceph |
| algOS | public | needs a clean one: both clips were removed for privacy at release | 11 stills, no `## Screenshots` heading | algOS Ceph (proposes how) |
| tandem | public | needs one: the site teaser was dropped (it showed a retired adapter); a TUI clip fits | 4 images, no `## Screenshots` heading | tandem Ceph — **needs a request** |
| herdr-agent-tree | public | needs one: it renders a live sidebar tree | no images at all | **no owner yet** |
| verdigris | public | not applicable (colour scheme) | 3-column "gallery" table, not `## Screenshots`, 2-column | verdigris Ceph — **needs a request** |
| omarchy-verdigris-theme | public | not applicable (theme) | "Previews" section, to align | verdigris Ceph — **needs a request** |
| verdigris.nvim | public | not applicable (colorscheme) | 1 image | verdigris Ceph — **needs a request** |
| dotfiles | private | not applicable: his README spec asks for a mise dot diagram, not a clip | — | algOS Ceph |
| herdr-notifs-plus | private | not in scope until a visibility decision | none | — |
| rssify | public (profile) | not applicable for now (a Slack bot; nothing on screen to loop) | none | — |

## How this Task closes

Re-read each README on GitHub when its owner reports, tick the row with the commit, and complete when every in-scope row follows the pattern.
