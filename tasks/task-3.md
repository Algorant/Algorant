---
id: task-3
uid: 4f6c1fe0-535e-402c-9cf1-eca0d9988dd6
type: task
title: "02 — Tandem: keep public face current"
state: todo
references: ["https://github.com/Algorant/tandem"]
relatedFiles: ["/home/ivan/Projects/tandem/README.md"]
tags: ["public-readiness", "tandem"]
accord:
  status: "ready"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope and address the agreed blockers; verify documentation, licensing/attribution, setup and usage claims, and experimental limitations against repository behavior.", "Record applicable repository-native checks and any explicit validation gaps, then record Algorant's approval of the public-facing result or explicit keep-private/defer decision."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:18Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-12T01:50:18Z"
priority: "high"
---
## State

Algorant/tandem is PUBLIC, at release 0.16.3, with a docs site. The new logo (mark D, v2 corner fix) and favicon are on local branch site-logo-v2, unpushed and awaiting Algorant's preview approval. The 88 s teaser v3 is final in 4K (fframes task-25).

## Shippable means

The common bar in AGENTS.md, plus: the site and README carry the current brand, and the docs match current behavior.

## Crippling issues

1. Docs describe old behavior: tandem task-51 (pre-0.3.0 workspace layout) and task-67 (stale review-status text, install tag pins).
2. Board-integrity bugs a new user can hit: task-63 (provisional ID returned after a parallel sync), task-64 (refused mutation leaves a written record), task-65 (no supported way to drop an unsynced record after migrate).
3. Brand is half-switched: the old mark is still in the home hero and social card; no light-theme variant; no slot for the teaser video.

## Next step

Algorant: approve the site-logo-v2 preview. Then the tandem Ceph pushes it, replaces the hero and social-card marks, and embeds the teaser.
