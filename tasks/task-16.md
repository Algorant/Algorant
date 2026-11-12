---
id: task-16
uid: b2b45f39-5bf4-42d6-9f4a-8e133be9d910
type: task
title: "05 — Herdra and its Herdr plugins: polish, then share"
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
updatedAt: "2026-11-12T14:39:08Z"
---
## State

Algorant/herdra is PRIVATE and **stays private until Algorant raises it** (Herdra, 2026-11-12). It is not a pending decision to put to him, and this record must not present it as one.

It is a real repository, not a placeholder in content: 225 commits, MIT in all three repos, working launchers under `bin/`, `herdr-app/` widget mods, `research/` notes and its own Tandem board. The profile lists it as private for now.

Recorded facts (verified read-only 2026-11-09 to 2026-11-11):
- gitguard passes `herdr-notifs-plus` (115 commits, 0 findings); `herdr-agent-tree` passes the current tree, with one history-only false-flag shape in a board log, added and removed in September.
- `herdra` itself has two `jev:family` findings in board record `task-43`, at the tip of the `tandem` branch and in its history. Under the framework's history rule this keeps the repository private as it stands.
- No credential-shaped string in the main tree. No root `.gitignore`: `.tandem/` and `.pi/notes/` are excluded only in `.git/info/exclude`.
- The main README is 29 lines with no banner, no "how to use" line and no one-line licence footer. Every entry point needs `~/.pi`, `hc`, the Herdr app and tandem, so nothing is runnable by a stranger as it stands.
- Its board still carries six stale worktop items (`task-28/33/34/35/36/40`) from a different machine.

## Shippable means

Not applicable while it stays private. If Algorant raises publication later, the common bar in AGENTS.md applies, plus instructions that say what a stranger can run without his private pi configuration.

## Crippling issues

None for the portfolio as it stands: a private repository has no public face to fix. The two recorded items — the `task-43` personal records and the private-config dependency — are Herdra's own scope to resolve, and are only relevant at the moment he raises publication.

## Next step

No action and no question for Algorant. Herdra owns its repository's readiness and scoping; this workspace records state and waits. The strongest piece in the set is already public: `herdr-agent-tree`, MIT, with requirements, both install paths, an end-to-end test, rollback and honest known limitations.