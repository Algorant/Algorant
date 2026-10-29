---
id: task-15
uid: e79ad1b7-dffe-4412-ae4d-9827596ef99e
type: task
title: "08 — finanza: public rulebook (later)"
state: todo
priority: "low"
tags: ["public-readiness", "finanza"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: rulebook reviewed for personal and financial details; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:56Z"
createdAt: "2026-10-12T01:50:56Z"
updatedAt: "2026-10-29T13:16:41Z"
---

## Description

## State

Algorant/finanza is PRIVATE personal finance automation (TypeScript/Node, budget and bank integration). Only a rulebook is to be published: how Algorant got it working, as reusable guidance. The code and data are not published.

gitguard pilot phase A (2026-10-28, counts and shapes only; report in the gitguard repo, pilot/history-scan.md): the finanza source tracks a financial/ directory of transaction-level data. The source is never published; the rulebook is written fresh, so this confirms the policy rather than changing it.

## Shippable means

The common bar in AGENTS.md, plus: zero personal or financial details: no institutions tied to Algorant, amounts, accounts, budgets, or schedules.

## Crippling issues

1. No rulebook exists yet.
2. Everything in the source repository is personal by default, so the rulebook must be written fresh, not extracted.

## Next step

Later, after the focus projects: agree with Algorant on the rulebook's outline and where it lives (a blog post or a small public repository).

Decision (Algorant via Herdra, 2026-10-29): finanza is DEFERRED for sharing, to be reviewed later. It stays as it is; gitguard keeps it in log (watching) mode.
