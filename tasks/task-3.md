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
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:58Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-26T03:53:49Z"
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

Visibility: public.

## Shippable means

The common bar in AGENTS.md, plus: the site and README carry the current brand, and the docs match current behavior.

## Crippling issues

1. Infrastructure details on the public repository (see scan). The tailnet name grants no access, but it and the username paths should stop appearing.

Remaining active project work (parent-closure assistance, deferred multi-project web, release-checklist wording, mise release pickup lag and small tooling papercuts) is not by itself a public-shipping blocker.


## Next step

Question with Algorant via Herdra (2026-10-26): have the tandem Ceph remove .tandem_old/ from main and stop writing MagicDNS URLs and home paths into board records, without a history rewrite (recommended). Held until his answer.
