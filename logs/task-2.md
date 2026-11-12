---
id: task-2
uid: dae194be-bd7a-4d67-9192-1b94ddd630c6
type: task
title: "02 — Pi catalog: polish, then share"
references: ["https://github.com/Algorant/pi"]
relatedFiles: ["docs/pi-public-mirror-plan.md", "docs/public-readiness.md", "README.md"]
tags: ["public-readiness", "pi"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-11-12T19:56:07Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-11-12T19:56:07Z"
priority: "high"
archivedAt: "2026-11-12T19:56:07Z"
resolution:
  outcome: "completed"
  note: "pi shipped: public since 2026-11-10 on a fresh history, README is the reference implementation of repo-style-rules, MIT detected, publisher green, gitguard 0 findings. Follow-ups live on .pi's board (task-668 to 671) plus a scan of the republished history."
---
## State

Algorant/pi is PUBLIC (flipped 2026-11-10; `gh repo view` reports `visibility: PUBLIC`). The public catalog is generated from the private source Algorant/.pi and was republished on a **fresh history**: 19 commits, tip `Update generated Pi snapshot` 2026-11-12 04:34, and the publisher Action is green on every recent push.

Verified 2026-11-12:
- README conforms to Algorant's repo-style-rules and is the reference implementation of them: `docs/banner.svg` as the title, two-sentence first-person intro, "How to use this repo" with the prohibition first, Core setup hierarchy, one line per extension, `## License` with `[MIT](LICENSE)`.
- LICENSE present at the root and GitHub reports MIT. The profile's "My Pi Setup" link now resolves for an anonymous visitor.
- Nothing machine-local is published: sessions, sdk, npm cache, settings, auth, memory and boards never enter the tree.
- gitguard passed the `.pi` source at `ca144380` (3271 commits, 68 refs, 0 findings) and the catalog before the republish (`4a525ef`, 252 commits, 0 findings).

About metadata is still empty (no description, homepage or topics).

## Shippable means

Met. The common bar in AGENTS.md, plus the README explaining the catalog model; the pending codemode refactor is stated as a known limitation on the board rather than in the README, which his repo-style-rules prefer.

## Crippling issues

None. Open, none of them publication blockers:
1. The `.pi` board carries the follow-ups Herdra routed there (task-668 to 671): the household-member account name in `scripts/browse-signin`, the personal ops scripts' place in the catalog, the case-insensitive replacement rules, and the skills test-and-trim.
2. gitguard's pass predates the fresh-history republish; the current 19-commit public history has not itself been scanned.
3. Publisher rough edges: bun pinned to `1.4.2` in the workflow; per-file notes written outside the checkout, so an unparseable extension README never fails the build.
4. `skills/agency/SKILL.md` still links the private herdra repo — a dead link for a visitor until herdra changes.

## Next step

Shipped and live; this record now tracks maintenance rather than readiness. Next concrete action: one gitguard scan of the republished public history, and the About fields filled (description, homepage, topics) in the same pass as any README touch. Nothing here waits on Algorant.