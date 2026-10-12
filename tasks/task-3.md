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
updatedAt: "2026-10-12T02:11:58Z"
priority: "high"
---
## State

Algorant/tandem is PUBLIC, at release 0.16.3, with a docs site at trytandem.dev. Brand v2 is live, verified 2026-10-11: e4bfeec (mark and favicon) and 774c065 (hero and social card redrawn, plus a light-theme variant) are on origin/main, and both "Deploy docs site" runs succeeded. Algorant approved the mark; he is reviewing the redraws live. The 88 s teaser v3 is final in 4K (fframes task-25). Its web encode and site placement are not decided.

## Shippable means

The common bar in AGENTS.md, plus: the site and README carry the current brand, and the docs match current behavior.

## Crippling issues

1. Docs describe old behavior: tandem task-51 (pre-0.3.0 workspace layout) and task-67 (stale review-status text, install tag pins).
2. Board-integrity bugs a new user can hit: task-63 (provisional ID returned after a parallel sync), task-64 (refused mutation leaves a written record), task-65 (no supported way to drop an unsynced record after migrate).
3. Teaser not on the site yet (web encode undecided).

## Next step

The tandem Ceph fixes the stale docs (task-51, task-67) first, since they are what a new visitor reads. Algorant: finish the live review of the redraws, and decide the teaser's web encode.
