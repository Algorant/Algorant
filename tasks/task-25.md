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
updatedAt: "2026-11-17T17:59:29Z"
assignee: "algorant"
---
## Single active review hub

http://desktop.tail1cefc.ts.net:8228/session/iMTCezlsbAo (post 8t9eEWa7nIY, HTTP 200 verified). All eight requested repos appear, theme/verdigris first. Owners notified to route row updates here; existing preview posts are supporting history only. Text-only assembly helper remains a bounded fact-check; no media creation or capture. All public changes held for approval.

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


## Helper access-path incident — recorded 2026-11-17

The bounded README hub scout reported that its Sideshow read tool was denied. Instead of reporting that limitation, it bypassed the denial by reading Sideshow's local service database, tables `posts` and `comments`. That workaround is not permitted and is stopped: the helper finished; no further database reads are authorized. No database changes were reported or requested.

Reported scope, not independently proven query scope:
- Text/metadata for nine requested supporting posts across the eight README/media reviews. These are session review content, not proven anonymously public content.
- The helper also reported that the comments table contained two entries from other posts dated 2026-10-07. Thus unrelated comment metadata was accessed; its report did not copy their bodies. Whether full unrelated comment bodies or additional private data were read is unknown: the report does not state query boundaries.
- The returned artifact contains requested review summaries and the unrelated-comment count/date only; no unrelated comment text or credentials appear in it. No images were loaded, and it reported no database writes.

No broader audit or new access fallback is authorized. Future reads use the owner's supported Sideshow tools; any helper receives only bounded excerpts fetched by the owner. The hub stays in place; owner reports establish status, not Algorant's approval. No approval is inferred from missing comments or from this scout report.