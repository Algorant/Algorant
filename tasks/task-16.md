---
id: task-16
uid: b2b45f39-5bf4-42d6-9f4a-8e133be9d910
type: task
title: "09 — Herdra: review readiness for eventual public sharing"
state: todo
priority: "low"
references: ["https://github.com/Algorant/herdra"]
relatedFiles: ["VISION.md", "README.md", "docs/public-readiness.md"]
tags: ["public-readiness", "herdra"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md, including documented usable prerequisites without private-config access; independently verified from an anonymous view.", "Every profile or channel link to it resolves anonymously after publication; until then the approved private placeholder is explicitly recorded.", "Algorant's publication or deferral decision is recorded."]
  constraints: ["Each project's own agent makes its changes; this workspace only records public state and coordinates through Herdra.", "Do not change visibility, rewrite history, publish or copy private repository contents into this public board without explicit authorization."]
  updatedAt: "2026-10-16T13:11:33Z"
createdAt: "2026-10-16T13:11:33Z"
updatedAt: "2026-10-26T03:56:42Z"
---

## Description

## State

Algorant/herdra is PRIVATE. Algorant requested its addition to the public portfolio with the private repository linked deliberately as a placeholder; an anonymous request currently returns HTTP 404. Eventual public sharing is intended, not authorized by this listing.

Herdra is Algorant's front-door orchestrator: a Pi session coordinating per-project agents (Cephs) over Herdr, Tandem and an agent inbox. It passes up results, decisions and blockers and keeps one focused Now item at a time.

Read-only checks confirm the repository identity/visibility, main at 5457d3f (clean and even with origin/main), VISION.md, AGENTS.md, README.md, bin/herdra, bin/herdra-check, bin/herdra-open, bin/herdra-tui, bin/herdra-cutover, research/, and its Tandem board. No public-readiness review has been done. Publication mechanism remains undecided; do not assume the current private tree or history can be published unchanged.

## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- No licence; short README. Research notes and board history hold the tailnet name, LAN IPs, a homelab domain, about 100 machine-name lines and a username path (research/task-12.md, task-15.md, task-39.md; AGENTS.md). No credentials; no blob over 1 MB.

Licence decision (Algorant via Herdra, 2026-10-26): MIT, copyright Algorant, for repos missing a licence; requested from the owner via Herdra.

Why private: "private for the moment… will go public eventually" (Algorant via Herdra).

## Shippable means

The common bar in AGENTS.md, plus: instructions explain the Pi/Herdr/Tandem/inbox prerequisites and what a stranger can actually run without access to Algorant's private Pi configuration. Licensing and attribution cover scripts and borrowed material.

## Crippling issues

Unknown until reviewed. Candidate review areas, not confirmed findings: private paths and machine names in AGENTS.md, VISION.md and research notes; dependency on the private .pi configuration; current tree, full history and board-history exposure; documentation, licensing and attribution. The placeholder link's anonymous 404 is expected and explicitly approved, not evidence of readiness.

## Next step

Herdra owns and scopes the research/ review itself (2026-10-26), including whether research/ and the board history can be public or need a fresh repository. Algorant decides timing.
