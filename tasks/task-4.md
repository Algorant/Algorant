---
id: task-4
uid: 65bf0b8b-f1b6-45e8-b6eb-028665166e14
type: task
title: "01 — Verdigris: public; keep public face current"
state: todo
references: ["https://github.com/Algorant/verdigris", "https://github.com/Algorant/omarchy-verdigris-theme", "https://github.com/Algorant/verdigris.nvim"]
tags: ["public-readiness", "verdigris"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:57Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-27T02:33:46Z"
priority: "high"
---
## State

Both repositories are PUBLIC. Verified 2026-10-26, logged out:
- **Algorant/verdigris** (palette and 15 terminal/editor/desktop ports): public since 2026-10-26, with Algorant's explicit OK via Herdra. The page returns HTTP 200 and an anonymous HTTPS clone works. main is one fresh commit (e8b8a39, "Initial Verdigris palette and theme ports"), and the tandem branch is a fresh one-commit board. MIT LICENSE, copyright 2026 Algorant. The README has no TODO left. Tree and board have no tailnet name, home paths or machine names. README links resolve: omarchy-verdigris-theme and verdigris.nvim are both public.
- **Algorant/omarchy-verdigris-theme**: public since 2026-10-15, MIT. The stale private-install paragraph is gone (cac3587).
- The full old history is kept PRIVATE in Algorant/verdigris-archive (anonymous 404), so the first name in old Windows-path commits is not public.

The profile's Verdigris link now resolves for visitors.

## Shippable means

The common bar in AGENTS.md, for each repository, plus:
- the main README shows screenshots of the main ports and links verdigris.nvim;
- the theme installs from its public HTTPS URL with `omarchy theme install`.

## Crippling issues

None verified. This check covered publication, licence, links and a sensitive-pattern check of the new public tree and board; it did not judge README screenshots or port quality.

## Next step

Keep the public face current: the verdigris Ceph reports significant changes through Herdra. Verdigris-archive stays private; publishing it would need its own explicit OK from Algorant.
