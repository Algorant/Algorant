---
id: task-13
uid: 6f9ff1e9-1bcb-4f15-821a-c46dd8b078b0
type: task
title: "05 — Algomarchy: public guide to customizing Omarchy"
state: todo
priority: "medium"
tags: ["public-readiness", "algomarchy"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: a section-per-area guide; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:53Z"
createdAt: "2026-10-12T01:50:53Z"
updatedAt: "2026-10-26T01:51:15Z"
---

## Description

## State

Algorant/Algomarchy is PRIVATE. It holds README.md (where each piece lives), CHECKLIST.md (new-machine bring-up), and an agent bootstrap skill, all written for Algorant's own machines. No public guide exists yet. Since 2026-10-11 the profile's Dev Setup/Tools list links Algorant/Algomarchy in place of AlgoNix (a dead link for visitors until the guide is public; Algorant accepts that as motivation). The planned guide is a checklist with one section per important part of Omarchy, covering how Algorant customized it.

## Shippable means

The common bar in AGENTS.md, plus: a section per major Omarchy area (e.g. packages, theme and Verdigris, keybindings, terminal and shell, mise bootstrap, agents) that explains what was changed. The generated dotfiles repository stays private (task-12), so the guide cannot rely on links into it.

## Crippling issues

1. No public artifact or format decision yet: a public subset of the repository, a generated guide, or blog posts.
2. Current docs mix in machine-specific and security-adjacent details (host names, pass-cli and SSH secret plumbing, drive layout) that must stay out.
3. The generated dotfiles stay private (Algorant's decision, task-12), so the guide must show the relevant configuration itself, for example with excerpts that pass the same privacy review.

## Next step

Waiting on Algorant: the guide's form is not decided yet (2026-10-11). Once decided, the Algomarchy Ceph drafts an outline of sections for review. When the guide's home is known, repoint the profile link if needed.

