---
id: task-9
uid: 4f1d3867-c431-4fd9-b300-737673aa6e7f
type: task
title: "07 — mediafetch: prepare for public sharing (later)"
state: todo
references: ["https://github.com/Algorant/mediafetch"]
tags: ["public-readiness", "mediafetch"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:51:01Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-16T12:52:24Z"
priority: "low"
---
## State

Algorant/mediafetch remains PRIVATE and testing/unaccepted. Independently verified: main at 2968a67 (approved vision and restart plan), clean and even with origin/main; latest GitHub release is still the historical 0.1.3 prerelease from 2026-09-29. No new release or native acceptance is established by the restart.

The goal remains a portable Obsidian media-note plugin across eight media types with narrowed providers. The approved direction is autonomous diagnosis outside Obsidian using the existing workbench and Obscura before handing Algorant a verified candidate. The current board consolidates work into task-1 (capability/readiness review), task-3 (vault-integration specification aligned with obsmd and Pi writers), task-47 (11-checkpoint diagnosis/repair loop), and task-46 (final desktop native acceptance). The old Windows/frozen-0.1.3 installation prerequisite is superseded, not an outstanding gate. The project owner reports review/spec Workers underway; their output is not yet acceptance evidence.

## Shippable means

The common bar in AGENTS.md, plus: installable through BRAT from the public repository, with an honest provider/credential matrix. A replacement candidate must pass the project's current release gates, outside-Obsidian workflow checks and content-preservation checks, then targeted native desktop acceptance. Harness success alone does not prove native Obsidian behavior, mobile support or accessibility.

## Crippling issues

1. No verified replacement candidate or final native acceptance yet. Do not present the old 0.1.3 beta as newly accepted or ready because planning restarted.
2. Provider identity/artwork and host-correct credential behavior remain under the consolidated task-47 checkpoints; results must distinguish fixed local defects from evidenced upstream limitations and untested flows.
3. Current capability/security review and vault integration are not complete (task-1/task-3). Portable notes must preserve user-owned content and follow the approved integration contract, not an invented universal schema.
4. Workbench/README/provider guidance must match verified behavior (task-47-11) before public claims are refreshed.

## Next step

The mediafetch Ceph verifies the current-state review and integration specification, then executes the bounded task-47 repair loop and supplies one exact candidate with concise evidence. Algorant performs the final targeted desktop native acceptance under task-46. Keep portfolio readiness testing/unaccepted until those outcomes are verified; publication still requires his explicit approval. The portfolio focus order has not changed.
