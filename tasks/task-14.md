---
id: task-14
uid: 35ffc32d-c0d4-4963-8c8e-6f787da348bd
type: task
title: "06 — obsmd: stays private; generic setup guide later"
state: todo
priority: "low"
tags: ["public-readiness", "obsmd"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: sensitivity decision recorded and applied; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:54Z"
createdAt: "2026-10-12T01:50:54Z"
updatedAt: "2026-10-29T13:16:43Z"
---

## Description

## State

Decision (Algorant via Herdra, 2026-10-26): the Algorant/obsmd repository stays PRIVATE. Publication plan, if anything goes public: a separate, generic guide on how to set up vault maintenance the way he has (skills, scripts and so on), as a new repository with fresh content, not a copy of obsmd's history, with no secrets or personal content, MIT licensed (copyright Algorant). Not scheduled.

obsmd itself is a project-local Pi skill set for maintaining Obsidian vaults (books, movies, finance bills modules) plus devlog and agent-sync docs.


## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- **Critical:** commit afbfc8e (2026-05-01) added real personal financial statements and transaction exports under data/finance_inputs/; they were deleted in aaf72d4 (2026-07-22) but remain in history. The repository cannot be published with its current history.
- Medium: tailnet name (8 commits), LAN IPs, machine names and home paths in history and the board; two identity emails at .pi/skills/devlog/references/harvest.md:69.
- No licence; README is a short draft. No credentials found; no blob over 1 MB.

gitguard pilot phase A (2026-10-28, counts and shapes only; report in the gitguard repo, pilot/history-scan.md): commit afbfc8e is no longer reachable from any branch, but GitHub still serves it by SHA (72 files) as an unreachable commit. The repository is private and stays private, so this is not exposed. It is the reason the framework requires a new repository, never an in-place rewrite, before anything turns public.

Why private: "semi-sensitive information" (Algorant's portfolio kickoff); the scan confirms it.

## Shippable means

For the future guide: the common bar in AGENTS.md, plus generic instructions with no vault content, personal or financial data, or infrastructure details, and an MIT licence.


## Crippling issues

None for the plan; the guide does not exist yet. The obsmd repository's history (see scan) is why it stays private.


## Next step

None scheduled. The obsmd Ceph's sensitivity inventory (requested by Herdra) can inform what the guide covers when Algorant schedules it.

gitguard ENABLED on obsmd, rules only with Jev off (Algorant via Herdra, 2026-10-29).
