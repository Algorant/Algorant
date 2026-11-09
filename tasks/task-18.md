---
id: task-18
uid: dd82eec9-33f1-44a4-84c3-bde894645683
type: task
title: "Migration plan for six public repos (pi, dotfiles, Algomarchy, tandem, verdigris, herdra)"
state: "in-progress"
priority: "high"
effort: "large"
accord:
  status: "delivered"
  acceptance: ["One Sideshow post published covering all six repos in Algorant's order, each with public state, blockers, simplify/rescope items, shortest path, and the five-point readiness checklist marked met/missing/unknown with evidence", "Board-level rescope proposals named per project as suggestions for each owner, not applied", "Cross-repo themes and a proposed order of work included", "No public flip, push or other-repo edit made"]
  claimedAt: "2026-11-09T22:04:55Z"
  deliveredAt: "2026-11-09T22:14:57Z"
  summary: "Six-repo migration plan published as one Sideshow post: per-repo state, outstanding work, his questions, owner-directed board proposals, readiness matrix with gitguard evidence, cross-repo themes, order of work, and the decisions only he can make."
  evidence: ["Sideshow post http://desktop.tail1cefc.ts.net:8228/session/RcUrkMsFz1A (post /p/FvNXz4niQ3A), 12 surfaces: overview, production-path diagram, one section per repo in Algorant's order, readiness matrix, cross-repo themes, proposed order and nine decisions", "Per-repo sections carry done / outstanding / needs your details / board proposals for the owner / shortest path, as Herdra relayed", "Five-point matrix filled with evidence; gitguard column replaced by the gitguard Ceph's scan pass at current tips (6 clean, herdra 2 jev:family findings in task-43, herdr-agent-tree 1 history-only candidate, verdigris + theme governed by Algorant's 2026-10-29 decision)", "No repo, board, or visibility changed in any other project; all changes proposed to owners"]
  updatedAt: "2026-11-09T22:14:57Z"
createdAt: "2026-11-09T22:04:46Z"
updatedAt: "2026-11-09T22:14:57Z"
assignee: "algorant"
---
## Algorant's words (verbatim)

"I want to reopen Algorant and, in light of all the recent changes, get an idea of how we migrate all the things we are working on. a few tasks can be simplified, and a few things can be rescoped, at the intersection of me wanting to make my repos public starting with 1) pi setup 2) dotfiles setup 3) Algomarchy guide 4) tandem 5) verdigris 6)herdra. some of these are already public and some are planned to be public but I mean seeing and reorganizing around what I can do to make them all simple, straightforward, public, and ready to go"

## "Ready to go public" (Algorant, via Herdra 2026-11-09, verbatim)

"that means organized nice readme, licence (always generic MIT no fuss), gitguard approved/passed, and having the latest updtaes along with confirming that private -> public actions work appropriately and consistently"

Five-point checklist per repo (README, MIT, gitguard, current, mechanism), marked met / missing / unknown with evidence. Herdra's format instruction: each repo gets its own section — what's done, what's outstanding, a short "needs your details" list — with the plan open-ended where Algorant's input is needed ("there are many things that won't be 'checklist'able until I give specific details for each repo"). Repos are then taken one at a time, in his order.

## Result (2026-11-09)

Sideshow post "Six repos: one migration plan", 12 surfaces: overview, production-path diagram, one section per repo in his order, readiness matrix, cross-repo themes, proposed order + the decisions only he can make.
- local: http://localhost:8228/session/RcUrkMsFz1A
- remote: http://desktop.tail1cefc.ts.net:8228/session/RcUrkMsFz1A (HTTP 200 verified)
- post: /p/FvNXz4niQ3A

## Headline findings, verified read-only

- **pi**: publisher green (last run 2026-11-09 22:01) and the catalog is byte-identical to `.pi` HEAD; gitguard passes both repos at tip (0 findings, full history). Outstanding: case-sensitive replacement rules (Archbox survived), homelab paths, no status line, bun pinned to 1.4.2, one dead link; and a judgement call on an account name in `scripts/browse-signin` (household member's first name; gitguard did not flag it, the framework counts family names as personal records).
- **dotfiles**: generated mirror is 115 commits behind `.dotfiles@omarchy` (29 files missing, 8 stale, 23 differ). Pipeline problem, not a visibility one.
- **Algomarchy guide**: `omarchy-setup` is the intended public repo but the profile links the private ops repo; `bootstrap.sh` defaults to the private (and stale) dotfiles mirror; 7 of 12 README images missing; an internal gate sentence still in the README.
- **tandem**: public, 0.17.5, docs match the CLI, gitguard clean; README lacks status/screenshot/known-issues/report path, repo About empty, and the public `tandem` branch is the internal work log (156 files, 381 commits).
- **verdigris**: public, MIT, clean; but 12 of 15 documented ports ship no artifact and point at private dotfiles; contributor push-guard needs a private literals file; previews show private project names.
- **herdra**: real 225-commit repo, not a placeholder in content; nothing runnable by a stranger; 2 `jev:family` findings in board record `task-43` at tip and in history (hard blocker); no root `.gitignore`; six stale worktop tasks.
- **gitguard scan pass at current tips** (8 repos, 0.5.1, Jev full, 0 unscanned): pass on `.pi`, the catalog, tandem, omarchy-setup, the generated dotfiles and herdr-notifs-plus; herdra as above; herdr-agent-tree one history-only false-flag shape needing Algorant's accept; verdigris + theme unscanned by Algorant's own 2026-10-29 decision.

## Boundaries honoured

No repo, board or visibility was changed in any other project; all board-level proposals are addressed to each owner in the post. Nothing flips without Algorant's explicit word at that moment. Questions were routed through Herdra.