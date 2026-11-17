---
id: task-25
uid: 3ac5f91c-c47f-4dc6-ad32-b11b4a107273
type: task
title: "README pattern A: demo first, Screenshots section last, per repo"
state: todo
priority: "high"
effort: "medium"
relatedFiles: ["VISION.md", "docs/public-readiness.md"]
accord:
  status: "ready"
  acceptance: ["Every in-scope public or going-public repo has its demo right after the intro, or is marked not applicable", "Each has a '## Screenshots' section near the end: same-size stills, 2-column table, small captions", "Each row is ticked with the commit that landed it, verified on GitHub"]
  updatedAt: "2026-11-17T15:38:09Z"
createdAt: "2026-11-17T15:38:09Z"
updatedAt: "2026-11-17T15:38:09Z"
---

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
