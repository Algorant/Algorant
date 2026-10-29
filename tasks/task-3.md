---
id: task-3
uid: 4f6c1fe0-535e-402c-9cf1-eca0d9988dd6
type: task
title: "02 — Tandem: keep public face current"
state: todo
references: ["https://github.com/Algorant/tandem"]
tags: ["public-readiness", "tandem"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:35Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-29T03:13:35Z"
priority: "high"
---
## State

Algorant/tandem is PUBLIC, at release 0.17.3 (published 2026-10-21), with the seven-page docs site live at trytandem.dev. Independently verified: origin/main at 66a87b0 (lock refresh after the fe0f417 release commit), 13 release assets, the release and site respond anonymously with HTTP 200, the docs deployment at 66a87b0 succeeded, and AUR tandem-bin is 0.17.3-1. Protocol remains 0.5.0; existing boards need no migration.

0.17.3: fresh workspaces start with six categorized starter rules, and any rule can be turned off and on without deletion (CLI `tandem rules enable/disable`, TUI keyboard/mouse; disabled rules remain visible via `tandem rules list --all`). Idle TUIs no longer rebuild board trees from unchanged Git snapshots every two seconds.

0.17.2 (2026-10-19): board commits use the repository's Git identity instead of a fixed Tandem author, so remotes with author push rules accept board syncs.

Earlier: 0.17.1 rewrote the docs into seven pages (Home, Quickstart, Concepts, Agents, TUI and web, CLI, Configuration) with diagrams, real captures, old-URL redirects and the teaser; it also fixed refused-mutation writes and concurrent-add IDs. 0.17.0 added the session working set and local-record activity chooser (not live agent/process monitoring). The new mark and site art are live.

## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- PUBLIC repository. The real tailnet name appears in 31 commits, including current board records; username home paths in the tracked .tandem_old/ folder on main (13 lines) and in 84 history commits. MIT licence. No credentials; no blob over 1 MB.

gitguard pilot phase A (2026-10-28, counts and shapes only; report in the gitguard repo, pilot/history-scan.md): 2 tailnet groups (59 occurrences) in board events and logs; home paths from 2 usernames in this clone. Cleanup is with the tandem Ceph (approved 2026-10-26).

Visibility: public.

## Shippable means

The common bar in AGENTS.md, plus: the site and README carry the current brand, and the docs match current behavior.

## Crippling issues

1. None open in the current tree or active board. Tailnet names and home paths remain only in history and archived board records, which are accepted by never-6 (no history rewrite).

Remaining active project work (parent-closure assistance, deferred multi-project web, release-checklist wording, mise release pickup lag and small tooling papercuts) is not by itself a public-shipping blocker.


## Next step

Cleanup check (2026-10-29):
- Main a164f66 removed .tandem_old/ (0 entries).
- Rule never-6 bans private hostnames, tailnet URLs, LAN IPs and absolute home paths in board records.
- The current board's active records are clean. The tailnet name remains only in 16 archived logs and 1 event file; home paths only in 11 archived logs. never-6 leaves archived records unchanged, so this is accepted history.
- Fixed: edb1ab8 (2026-10-29) replaced the 13 real-username absolute home paths on main with ~/… paths, no history rewrite. Verified from an anonymous clone: no real-username home paths and no tailnet name in the main tree.
