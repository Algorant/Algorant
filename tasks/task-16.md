---
id: task-16
uid: b2b45f39-5bf4-42d6-9f4a-8e133be9d910
type: task
title: "6 — herdra: private until Algorant raises it (no action)"
state: todo
priority: "high"
references: ["https://github.com/Algorant/herdra"]
relatedFiles: ["VISION.md", "README.md", "docs/public-readiness.md"]
tags: ["public-readiness", "herdra"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md, including documented usable prerequisites without private-config access; independently verified from an anonymous view.", "Every profile or channel link to it resolves anonymously after publication; until then the approved private placeholder is explicitly recorded.", "Algorant's publication or deferral decision is recorded."]
  constraints: ["Each project's own agent makes its changes; this workspace only records public state and coordinates through Herdra.", "Do not change visibility, rewrite history, publish or copy private repository contents into this public board without explicit authorization."]
  updatedAt: "2026-10-16T13:11:33Z"
createdAt: "2026-10-16T13:11:33Z"
updatedAt: "2026-11-12T19:56:46Z"
---
## State

`Algorant/herdra` is private and **stays private until Algorant raises it** — not a pending decision, and never something to put to him.

Real repository, not a placeholder in content: 225 commits, MIT, `bin/` launchers, `herdr-app/` mods, `research/`, its own board. Its public plugin `herdr-agent-tree` is a strong public artifact (requirements, both install paths, e2e test, rollback, known limitations); `herdr-notifs-plus` is private, MIT, gitguard clean (115 commits).

Recorded, for the moment he raises it: two `jev:family` findings in board record `task-43` (tip and history); no root `.gitignore`; nothing runnable by a stranger (every entry point needs `.pi`, `hc`, the Herdr app and tandem); six stale worktop cards on its board.

## Next step

None here. Herdra owns its own readiness and scoping; this card records state.

## Waiting on

Nothing — and no question for Algorant.