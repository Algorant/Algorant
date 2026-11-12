---
id: task-4
uid: 65bf0b8b-f1b6-45e8-b6eb-028665166e14
type: task
title: "04 — Verdigris: polish, then share"
state: todo
references: ["https://github.com/Algorant/verdigris", "https://github.com/Algorant/omarchy-verdigris-theme", "https://github.com/Algorant/verdigris.nvim"]
tags: ["public-readiness", "verdigris"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:37Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-11-12T14:42:55Z"
priority: "high"
---
## State

Both repositories are PUBLIC: `Algorant/verdigris` (palette, fresh history since 2026-10-26) and `Algorant/omarchy-verdigris-theme` (public since 2026-10-15). The old history stays private in `verdigris-archive`. MIT in both.

**Goal (Algorant, via Herdra 2026-11-12, his words):** "its mean to be a public colorscheme repo where people can see waht I use for config, with pictures/demos of what they look like for every given thing piece of software etc." Modelled on kepano's flexoki: a palette, a real theme file, and a screenshot per supported app.

**Rescoping with its Ceph** (terminal t41), which owns the plan (Sideshow "verdigris rescope"). This workspace records state only; it does not scope or critique the repo's contents. Algorant's correction, worth keeping in mind: cataloguing what is private today misses the point of the repo.

Verified 2026-11-12:
- The palette is shown plainly: SVG swatch plus a hex table.
- The Omarchy theme carries previews, an install command, what-gets-themed and the palette mapping; every README link resolves.
- Both trees are clean and both boards are empty.
- gitguard adopted after Algorant's 2026-11-09 answer and **passing**: `6aa49f7` (22 commits, 7 refs) and `2c9ba58` (13 commits, 3 refs), 0 findings, with its Ceph chaining gitguard into the repo's existing tracked guard and proving it with planted-secret and financial-path pushes.

## Shippable means

The common bar plus the goal above: for every supported piece of software, something a visitor can see and use — a theme file and a screenshot, not a description of where a file might live.

## Crippling issues

None recorded here. Content and shape are the rescope's business; this record does not grade them.

## Next step

Wait for its Ceph's rescope plan and report; update the state here when it lands. Nothing waits on Algorant.