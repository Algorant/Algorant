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
updatedAt: "2026-10-16T12:39:20Z"
priority: "high"
---
## State

Algorant/tandem is PUBLIC, at release 0.17.1 (published 2026-10-16), with rewritten documentation live at trytandem.dev. Independently verified: main is at 2736599 (Release Tandem 0.17.1), GitHub lists 13 release assets, the release responds anonymously with HTTP 200, and AUR tandem-bin is 0.17.1-1. Herdra reports asset checksums verified; this portfolio check did not repeat the downloads/checksum audit. Protocol remains 0.5.0; current boards need no migration.

The seven-page docs/site overhaul is shipped, no longer paused: Home, Quickstart, Concepts, Agents, TUI and web, CLI, Configuration. All seven public routes returned HTTP 200. Live Concepts includes board storage and independent sync, diagrams and real product captures. The source has 12 old-URL aliases; the live /workspace/ alias points to /concepts/#board-storage-and-sync. The docs deployment at 190ad10 succeeded. The homepage now links the teaser, and its MP4 responds with HTTP 200: the earlier missing-teaser blocker is resolved.

Release notes describe refused mutations checked before record writes, correct published IDs on concurrent adds, protocol-shaped structured event data, and `$ ` runnable-validation help. Herdra also reports stricter release gates. Tandem task-63 and task-64 are archived completed; task-76 (docs overhaul) is archived completed. Task-65 was canceled because pre-0.5 boards are unsupported and live boards are current, not because a general repair feature shipped.

The 0.17.0 session working set and local-record activity chooser remain part of the shipped product; the chooser is not live agent/process monitoring. The new mark, light-theme variant and site art are live.

## Shippable means

The common bar in AGENTS.md, plus: the site and README carry the current brand, and the docs match current behavior.

## Crippling issues

No currently verified public-facing crippling issue from the previous list remains: the stale docs, refused-write/concurrent-ID bugs and missing teaser have been addressed; the old migration case is explicitly unsupported. This is a portfolio verification of publication, contents and board outcomes, not a new full-history safety audit or exhaustive functional test.

Remaining active project work (rules UX, parent-closure assistance, deferred multi-project web, and release-checklist wording) is not by itself a public-shipping blocker.

## Next step

The tandem Ceph keeps docs and release descriptions aligned with shipped behavior and surfaces any newly verified public-facing blocker through Herdra. The portfolio record no longer waits for docs-overhaul approval, deployment or teaser placement.
