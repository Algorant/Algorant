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
updatedAt: "2026-10-12T20:38:40Z"
priority: "high"
---
## State

Algorant/tandem is PUBLIC, at release 0.17.0 (published 2026-10-12), with a docs site at trytandem.dev. Independently verified: main at 1f8b59a (Release Tandem 0.17.0), public GitHub release and site respond anonymously with HTTP 200, and AUR tandem-bin is 0.17.0-1.

0.17.0 adds an in-memory session working set: switching between boards opens each board's full TUI, and the chooser shows local Task counts and bounded in-progress work. The overview reflects board records, not live agent/process status or remote freshness. No migration; protocol remains 0.5.0. Also shipped: external-blocker guidance, optional archive resolution notes, and the new mark/favicon, hero/social card and light-theme logo variant.

Algorant approved the mark; final live redraw review has not been confirmed here. The 88 s teaser v3 is final in 4K (fframes task-25); web encode and site placement remain undecided.

## Shippable means

The common bar in AGENTS.md, plus: the site and README carry the current brand, and the docs match current behavior.

## Crippling issues

1. Stale docs and incomplete coverage of shipped behavior. The paused docs/site overhaul (tandem task-76) absorbs task-51's old workspace-layout text and task-67's review-status, Validation and install/version guidance. Its approved seven-page shape is not deployed.
2. Board-integrity issues remain on Tandem's active board: task-63 (provisional ID returned after a parallel sync), task-64 (refused mutation leaves a written record), task-65 (no supported way to drop an unsynced record after migrate).
3. Teaser not on the site yet (web encode undecided).

## Next step

Keep the docs overhaul paused until Herdra's style guide is ready and owner direction authorizes resumption (task-76); the revised TUI working-set features have now shipped. The tandem Ceph then updates docs for 0.17.0 within the approved seven-page shape and brings the rendered result to Algorant for approval before integration/deployment. Algorant decides final redraw review and teaser web encode/site placement.
