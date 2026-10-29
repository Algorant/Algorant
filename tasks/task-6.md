---
id: task-6
uid: d883b64e-698b-4484-a310-558ddefcc277
type: task
title: "09 — xunfurl: prepare for public sharing (not in focus)"
state: todo
references: ["https://github.com/Algorant/x_unfurl"]
tags: ["public-readiness", "x_unfurl"]
accord:
  status: "ready"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope and address the agreed blockers; verify documentation, licensing/attribution, setup and usage claims, and experimental limitations against repository behavior.", "Record applicable repository-native checks and any explicit validation gaps, then record Algorant's approval of the public-facing result or explicit keep-private/defer decision."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:39Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-29T03:47:10Z"
priority: "low"
---
## State

Linked from the profile README but not in the current focus (VISION.md). GitHub: https://github.com/Algorant/x_unfurl. Checkout: ~/Projects/x_unfurl (not present on every machine). Not reviewed since the original inventory.

## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- No licence. .env.example holds placeholder Slack tokens only. No credentials.

Why private: no recorded reason.

## Next step

None until Algorant brings it into focus.
