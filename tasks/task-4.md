---
id: task-4
uid: 65bf0b8b-f1b6-45e8-b6eb-028665166e14
type: task
title: "04 — Verdigris: polish, then share"
state: todo
references: ["https://github.com/Algorant/verdigris", "https://github.com/Algorant/omarchy-verdigris-theme", "https://github.com/Algorant/verdigris.nvim"]
tags: ["public-readiness", "verdigris"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:37Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-11-12T14:42:00Z"
priority: "high"
---
## State

Both repositories are PUBLIC: `Algorant/verdigris` (palette, fresh history since 2026-10-26) and `Algorant/omarchy-verdigris-theme` (public since 2026-10-15). The old history stays private in `verdigris-archive`. MIT in both.

**Rescoped by Algorant (2026-11-12, via Herdra): verdigris is a public colour scheme repo, in the spirit of flexoki.** Its own Ceph plans the work, so this workspace records state only and does not critique or scope its contents.

Verified 2026-11-12:
- The palette is shown plainly: SVG swatch plus a hex table, with the extended colours one link away.
- The Omarchy theme carries previews, an install command, what-gets-themed and the palette mapping; every README link resolves.
- Both trees are clean and both boards are empty (their work is archived).
- gitguard adopted after Algorant's 2026-11-09 answer and **passing**: `6aa49f7` (22 commits, 7 refs) and `2c9ba58` (13 commits, 3 refs), 0 findings. Its Ceph chained gitguard into the repo's existing tracked guard, proved it with planted-secret and financial-path pushes, and left only wallpaper and preview images unverified by eye.
- No tags or releases in either repo; the palette version lives only in `css/palette.json` (0.2.0).

## Shippable means

Met as visibility, and the rescope sets the content bar. What the public face still lacks, recorded for its Ceph rather than as a request to anyone: a banner, the one-line licence footer from his repo-style-rules, and a version story (the palette is at 0.2.0 and nothing is tagged). Preview images still carry internal context (`previews/herdr.png` lists private project names and task ids; `btop.png` shows exact hardware). The HTTPS theme install is documented but was never exercised on this machine, and `verdigris-archive` is undocumented.

## Crippling issues

None. Both repos are public, clean and scanning clean.

## Next step

Its Ceph plans the colour-scheme shape; nothing here waits on Algorant. This record updates when that Ceph reports.