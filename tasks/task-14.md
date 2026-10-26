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
updatedAt: "2026-10-26T03:53:20Z"
---

## Description

## State

Algorant/obsmd is PRIVATE. It is a project-local Pi skill for maintaining Obsidian vaults (books, movies, finance bills modules) plus devlog and agent-sync docs. Algorant wants it public, ideally the repository itself, but it contains semi-sensitive information.

## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- **Critical:** commit afbfc8e (2026-05-01) added real personal financial statements and transaction exports under data/finance_inputs/; they were deleted in aaf72d4 (2026-07-22) but remain in history. The repository cannot be published with its current history.
- Medium: tailnet name (8 commits), LAN IPs, machine names and home paths in history and the board; two identity emails at .pi/skills/devlog/references/harvest.md:69.
- No licence; README is a short draft. No credentials found; no blob over 1 MB.

Why private: "semi-sensitive information" (Algorant's portfolio kickoff); the scan confirms it.

## Shippable means

The common bar in AGENTS.md, plus: the sensitivity question is settled first, and nothing about the vault's personal content (finance, reading, people) is exposed in the tree or history.

## Crippling issues

1. Personal financial documents in history (see scan). Publishing needs a new repository with fresh, reviewed history, or a history rewrite.
2. Infrastructure details (tailnet, LAN IPs, machine names) in history and board.
3. No licence; the public subset is not defined.


## Next step

Herdra has asked the obsmd Ceph for a path/category inventory of sensitive material (2026-10-26). Question with Algorant via Herdra: publish from a new repository with fresh history, keeping the current one private (recommended). Then agree the public tree.
