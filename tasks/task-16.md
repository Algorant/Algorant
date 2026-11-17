---
id: task-16
uid: b2b45f39-5bf4-42d6-9f4a-8e133be9d910
type: task
title: "herdra: readiness review and public plan (private until his flip word)"
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
updatedAt: "2026-11-17T14:33:11Z"
---
## Raised by Algorant (2026-11-15, via Herdra)

"so as far as repos to make 'nice' we have tasks to fix dotfiles and herdra, and do a review of tandem, right?"

herdra is now an active readiness Task. It stays **private until his explicit flip word**; this card plans readiness, it does not authorize publication.

## What this Task needs

1. A review against the readiness bar (README in repo-style-rules, MIT, gitguard at tip, current, mechanism), with evidence at the current tip.
2. A public-readiness plan from that review, covering at least the recorded blockers below.

Owner of the review and changes: Herdra, for its own repository. Not started: Herdra dispatches it once Algorant confirms the order.

## Recorded blockers (read-only, 2026-11-09 to 11-12)

- Two `jev:family` gitguard findings in board record `task-43`, at the tip of the `tandem` branch and in its history; under the history rule the repository cannot go public as it stands.
- No root `.gitignore`; `.tandem/` and `.pi/notes/` are excluded only via `.git/info/exclude`.
- README has no banner, no "how to use" line and no one-line licence footer.
- Nothing runnable by a stranger: entry points need `~/.pi`, `hc`, the Herdr app and tandem.
- Tracked screenshots of live workflow (`herdr-app/*/shots/*.png`) and machine-specific `research/` notes.
- Six stale worktop cards on its board (`task-28/33/34/35/36/40`).

Plugins: `herdr-agent-tree` is public and strong; `herdr-notifs-plus` is private and scans clean.

## History

Until 2026-11-15 this card read "private until Algorant raises it (no action)". Prior body retained below.

---

## State

`Algorant/herdra` is private and **stays private until Algorant raises it** — not a pending decision, and never something to put to him.

Real repository, not a placeholder in content: 225 commits, MIT, `bin/` launchers, `herdr-app/` mods, `research/`, its own board. Its public plugin `herdr-agent-tree` is a strong public artifact (requirements, both install paths, e2e test, rollback, known limitations); `herdr-notifs-plus` is private, MIT, gitguard clean (115 commits).

Recorded, for the moment he raises it: two `jev:family` findings in board record `task-43` (tip and history); no root `.gitignore`; nothing runnable by a stranger (every entry point needs `.pi`, `hc`, the Herdr app and tandem); six stale worktop cards on its board.

## Next step

None here. Herdra owns its own readiness and scoping; this card records state.

## Waiting on

Nothing — and no question for Algorant.

## Media exception (Algorant, 2026-11-17, via Herdra)

Herdra screenshots showing his project list, a cost footer and agent transcripts were flagged and a retake proposed. He overrode that for these shots only: "I disagree with your 'retake'. I am the human for which the guard was created. I do not consider any of those a big deal. its fine" — and then: "not permanently, its good that gitguard found them or whatever you used, but I am overriding them as an exception".

One-off exception for this herdra media. The readiness bar is unchanged: his own information is still flagged in other reviews.