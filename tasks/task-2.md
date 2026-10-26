---
id: task-2
uid: dae194be-bd7a-4d67-9192-1b94ddd630c6
type: task
title: "03 — Pi setup: publish the generated catalog"
state: todo
references: ["https://github.com/Algorant/pi"]
relatedFiles: ["docs/pi-public-mirror-plan.md", "docs/public-readiness.md", "README.md"]
tags: ["public-readiness", "pi"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:59Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-26T03:13:10Z"
priority: "high"
---
## State

The private source is Algorant/.pi (checkout ~/.pi); last commit 2026-10-22 (43cf1b5). The "Publish Pi snapshot" Action regenerates Algorant/pi on every main push; the latest run succeeded and regenerated the catalog on 2026-10-22 (2128247). Verified 2026-10-26: Algorant/pi is still PRIVATE (top level: README.md, config-manifest.json, extensions, prompts, scripts, skills, themes), so the profile's "My Pi Setup" link 404s (kept on purpose by Algorant as motivation). No public-readiness review of the generated catalog appears on the .pi board.

Recent features: agent inbox, Herdra widget, model roles with quota-aware choice, an adversarial reviewer, dbs, /mem. Codemode is used throughout. Algorant expects a significant codemode-driven refactor, which does not block publishing.


## Shippable means

The common bar in AGENTS.md, plus: the public README explains the codemode-based tool model wherever it matters, and states the pending refactor as a known limitation.

Algorant keeps the dead profile link on purpose (2026-10-11), as motivation to get this public.

## Crippling issues

1. The generated Algorant/pi is private, so the link is dead.
2. The public README and output have not been reviewed since codemode, model roles, and the inbox landed. The codemode-awareness of the public text is unknown.
3. Open Worker and Subagent reliability bugs on the .pi board (task-405, task-409, task-410) affect anyone copying the delegation setup.
(Inferred read-only; not yet confirmed with the .pi Ceph.)

## Next step

Herdra has put a .pi Ceph readiness review to Algorant (2026-10-26): one review of a fresh clone of Algorant/pi covering safety, README and codemode/model-role/inbox accuracy. Record his answer and the review's findings, then Algorant decides visibility.
