---
id: task-3
uid: 4f6c1fe0-535e-402c-9cf1-eca0d9988dd6
type: task
title: "01 — Tandem: polish, then share"
references: ["https://github.com/Algorant/tandem"]
tags: ["public-readiness", "tandem"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-11-12T19:56:08Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-11-12T19:56:08Z"
priority: "high"
archivedAt: "2026-11-12T19:56:08Z"
resolution:
  outcome: "completed"
  note: "tandem shipped: 0.17.7 verified (tag tandem-v0.17.7), banner, rule-compliant README, About filled, planning trees removed, doc pins fixed, site 200. Only the AUR build remains (tandem task-104)."
---
## State

Algorant/tandem is PUBLIC, at 0.17.7 (tag `tandem-v0.17.7`, release 2026-11-11), MIT. Verified 2026-11-09 to 2026-11-11: the docs site at trytandem.dev returns 200 and is generated from `docs/`, the release carries the installer plus linux/darwin x86_64+aarch64 tarballs, every command in `tandem --help` appears in the CLI docs, and gitguard passes (0 findings at `121aee5`, 1054 commits, 65 refs; its Ceph reports 0 findings across 1,096 commits at the review tip).

The public face, after Algorant's cleanup review (`a356a45`, "Public face: README and banner, one docs owner, no planning trees"):
- README follows his repo-style-rules: `docs/banner.svg` as the title, two-sentence first-person intro, "How to use this repo" with the prohibition first, Core hierarchy, and `## License` with `[MIT](LICENSE)`. Status, screenshot and known-issues sections were declined by design.
- About filled: description "local-first coordination for people and agents, in plain Markdown", homepage https://trytandem.dev, eight topics.
- `plan/` trees, `tandem/plan`, `protocol/plan` and the empty `extensions/` placeholder are gone from the tree; the stale 0.17.1/0.17.3 doc pins are fixed; the site teaser was dropped because it showed a retired adapter.
- The `tandem` branch stays public by Algorant's decision (the board demonstrates the product), with board messages hostname-free going forward and existing history kept.

## Shippable means

The common bar in AGENTS.md, plus: the site and README carry the current brand, and the docs match current behavior.

## Crippling issues

1. AUR is the one missing install path: `tandem-bin` is stuck on the Arch openssl failure (tandem `task-104`), so the README names only the curl installer and cargo. Not a blocker for reading the repo, but a real gap for Arch users.
2. Accepted, recorded: the public `tandem` branch still carries the board's history with machine names, coordinator ids and internal project names from before the hostname-free rule. Under the narrowed framework this is publishable, and Algorant chose to keep the history rather than rewrite it.

Nothing else open: no README, licence, About, metadata or link problem remains on the public surface.

## Next step

tandem is the first project in the polish-then-share sequence: with the public face shipped, the remaining prerequisites are the AUR build (`task-104`) and a decision on when to announce (X thread, blog post, video). Its board carries the substantive work: `task-97` (complete delivers and accepts in one write) is the main agent-facing item; `task-75` and `task-42` are close-or-recheck candidates; `task-93` needs rewording because it sits on a public board.

My six-repo plan records tandem's state and points at this review: http://desktop.tail1cefc.ts.net:8228/session/RcUrkMsFz1A