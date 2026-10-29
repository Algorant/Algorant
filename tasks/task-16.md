---
id: task-16
uid: b2b45f39-5bf4-42d6-9f4a-8e133be9d910
type: task
title: "05 — Herdra and its Herdr plugins: polish, then share"
state: todo
priority: "high"
references: ["https://github.com/Algorant/herdra"]
relatedFiles: ["VISION.md", "README.md", "docs/public-readiness.md"]
tags: ["public-readiness", "herdra"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md, including documented usable prerequisites without private-config access; independently verified from an anonymous view.", "Every profile or channel link to it resolves anonymously after publication; until then the approved private placeholder is explicitly recorded.", "Algorant's publication or deferral decision is recorded."]
  constraints: ["Each project's own agent makes its changes; this workspace only records public state and coordinates through Herdra.", "Do not change visibility, rewrite history, publish or copy private repository contents into this public board without explicit authorization."]
  updatedAt: "2026-10-16T13:11:33Z"
createdAt: "2026-10-16T13:11:33Z"
updatedAt: "2026-10-29T03:47:43Z"
---

## Description

## State

Algorant/herdra is PRIVATE. Algorant requested its addition to the public portfolio with the private repository linked deliberately as a placeholder; an anonymous request currently returns HTTP 404. Eventual public sharing is intended, not authorized by this listing.

Herdra is Algorant's front-door orchestrator: a Pi session coordinating per-project agents (Cephs) over Herdr, Tandem and an agent inbox. It passes up results, decisions and blockers and keeps one focused Now item at a time.

Read-only checks confirm the repository identity/visibility, main at 5457d3f (clean and even with origin/main), VISION.md, AGENTS.md, README.md, bin/herdra, bin/herdra-check, bin/herdra-open, bin/herdra-tui, bin/herdra-cutover, research/, and its Tandem board. No public-readiness review has been done. Publication mechanism remains undecided; do not assume the current private tree or history can be published unchanged.

## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- No licence; short README. Research notes and board history hold the tailnet name, LAN IPs, a homelab domain, about 100 machine-name lines and a username path (research/task-12.md, task-15.md, task-39.md; AGENTS.md). No credentials; no blob over 1 MB.

Licence: MIT added (4afb212, 2026-10-26, verified).

Why private: "private for the moment… will go public eventually" (Algorant via Herdra).

## Shippable means

The common bar in AGENTS.md, plus: instructions explain the Pi/Herdr/Tandem/inbox prerequisites and what a stranger can actually run without access to Algorant's private Pi configuration. Licensing and attribution cover scripts and borrowed material.

## Crippling issues

1. Personal records: gitguard 0.5.0 (2026-10-29) found family members' names and account handles in Herdra's board record task-43, both at the current tip of the tandem branch and in its history. Under the framework's history rule, the repository stays private unless Algorant chooses another route. Herdra has the options from gitguard.

Done: MIT licence, the reference README note and the AGENTS.md section (49a5df6). The polish replace was skipped deliberately because the files are live operating instructions.

## Next step

Herdra owns and scopes the research/ review itself (2026-10-26), including whether research/ and the board history can be public or need a fresh repository. Algorant decides timing.

Upcoming (Algorant, 2026-10-29; not scoped, nothing started): significant presentability polish first, then sharing through X/Twitter threads, blog posts and videos. Any flip waits for Algorant (the 2026-10-29 flip list is on hold). Item 5 covers Herdra together with herdr-agent-tree (public, MIT) and herdr-notifs-plus (private, MIT).
