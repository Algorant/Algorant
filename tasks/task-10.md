---
id: task-10
uid: 6d6572a5-571c-4be2-a418-c7b86ae03e30
type: task
title: "13 — AlgoPDF: prepare for public sharing (not in focus)"
state: todo
references: ["https://github.com/Algorant/AlgoPDF"]
tags: ["public-readiness", "algopdf"]
accord:
  status: "ready"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope and address the agreed blockers; verify documentation, licensing/attribution, setup and usage claims, and experimental limitations against repository behavior.", "Record applicable repository-native checks and any explicit validation gaps, then record Algorant's approval of the public-facing result or explicit keep-private/defer decision."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:51:05Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-26T03:53:33Z"
priority: "low"
---
## State

Linked from the profile README but not in the current focus (VISION.md). GitHub: https://github.com/Algorant/AlgoPDF. Checkout: ~/Projects/AlgoPDF (not present on every machine). Not reviewed since the original inventory.

## Next step

None until Algorant brings it into focus.## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- GPL-2.0 licence with NightPDF attribution in the README. Secret-pattern hits are inside vendored yarn and pdf.js bundles (false positives). No credentials.

Why private: no recorded reason.


