---
id: task-9
uid: 4f1d3867-c431-4fd9-b300-737673aa6e7f
type: task
title: "07 — mediafetch: prepare for public sharing (later)"
state: todo
references: ["https://github.com/Algorant/mediafetch"]
relatedFiles: ["/home/ivan/Projects/mediafetch/README.md"]
tags: ["public-readiness", "mediafetch"]
accord:
  status: "ready"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope and address the agreed blockers; verify documentation, licensing/attribution, setup and usage claims, and experimental limitations against repository behavior.", "Record applicable repository-native checks and any explicit validation gaps, then record Algorant's approval of the public-facing result or explicit keep-private/defer decision."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:25Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-12T01:50:25Z"
priority: "low"
---
## State

Algorant/mediafetch is PRIVATE. The Obsidian plugin's 0.1.3 beta was declared for BRAT; native install testing is open (mediafetch task-46). It has many open provider-quality issues.

## Shippable means

The common bar in AGENTS.md, plus: installable through BRAT from the public repository, with the README listing the providers and their credential needs.

## Crippling issues

1. Provider identity and artwork gaps (mediafetch task-22, 32, 34, 35, 36, 43).
2. The README and validation guidance are stale after the provider rollout (task-37).
3. Credential and secret-storage review is open (task-2).

## Next step

Later, after the focus projects: the mediafetch Ceph finishes task-46 and task-37.
