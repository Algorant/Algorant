---
id: task-14
uid: 35ffc32d-c0d4-4963-8c8e-6f787da348bd
type: task
title: "06 — obsmd: decide what stays private, then publish"
state: todo
priority: "medium"
tags: ["public-readiness", "obsmd"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: sensitivity decision recorded and applied; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:54Z"
createdAt: "2026-10-12T01:50:54Z"
updatedAt: "2026-10-12T01:50:54Z"
---

## Description

## State

Algorant/obsmd is PRIVATE. It is a project-local Pi skill for maintaining Obsidian vaults (books, movies, finance bills modules) plus devlog and agent-sync docs. Algorant wants it public, ideally the repository itself, but it contains semi-sensitive information.

## Shippable means

The common bar in AGENTS.md, plus: the sensitivity question is settled first, and nothing about the vault's personal content (finance, reading, people) is exposed in the tree or history.

## Crippling issues

1. Unresolved sensitivity: the vault aliases and config, the finance-bills module, devlog harvests, and the agent-sync store layout may reveal personal data or infrastructure.
2. The repository history has not been reviewed.
3. Choice among gitignore, a private/public split, or a generated public subset is open.

## Next step

The obsmd Ceph inventories the semi-sensitive material by path and category (no values) and proposes gitignore, split, or subset. Then Algorant decides.

