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
updatedAt: "2026-10-27T04:17:01Z"
priority: "high"
---
## State

The private source is Algorant/.pi (checkout ~/.pi); last commit 2026-10-22 (43cf1b5). The "Publish Pi snapshot" Action regenerates Algorant/pi on every main push; the latest run succeeded and regenerated the catalog on 2026-10-22 (2128247). Verified 2026-10-26: Algorant/pi is still PRIVATE (top level: README.md, config-manifest.json, extensions, prompts, scripts, skills, themes), so the profile's "My Pi Setup" link 404s (kept on purpose by Algorant as motivation). No public-readiness review of the generated catalog appears on the .pi board.

Recent features: agent inbox, Herdra widget, model roles with quota-aware choice, an adversarial reviewer, dbs, /mem. Codemode is used throughout. Algorant expects a significant codemode-driven refactor, which does not block publishing.


## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- Generated Algorant/pi: no licence; README links the private Algorant/.pi source (dead for visitors); external links resolve. Machine names in docs and code by design (inbox, model roles, memory); a Windows vault path in skills/memory/SKILL.md:30. No credentials; no blob over 1 MB.

Licence decision (Algorant via Herdra, 2026-10-26): MIT, copyright Algorant; sent to the .pi Ceph to add through the publisher.

gitguard pilot phase A (2026-10-28, counts and shapes only; report in the gitguard repo, pilot/history-scan.md): the generated catalog's dbs skill docs and script name the homelab Postgres domain (an internal domain, so a leak; found only by Jev until a literal rule exists); 3 user-home path groups, one a real README example path; machine-name notes. To be fixed in the .pi source before any publication.

Why private: no recorded reason. The public-mirror plan authorized planning only and publication was never approved; the .pi source is private by design.

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
