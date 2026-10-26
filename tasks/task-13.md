---
id: task-13
uid: 6f9ff1e9-1bcb-4f15-821a-c46dd8b078b0
type: task
title: "05 — Algomarchy: public Omarchy guide (omarchy-setup)"
state: todo
priority: "medium"
tags: ["public-readiness", "algomarchy"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: a section-per-area guide; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:53Z"
createdAt: "2026-10-12T01:50:53Z"
updatedAt: "2026-10-26T03:13:07Z"
references: ["https://github.com/Algorant/omarchy-setup", "https://github.com/Algorant/Algomarchy"]
---

## Description

## State

The guide now lives in a separate, hand-maintained repository: Algorant/omarchy-setup (titled Algomarchy). It is PRIVATE; last commit 2026-10-19 (7a09a93). Verified 2026-10-26: its tree is README.md (the guide, with a three-step bring-up: install Omarchy, run bootstrap.sh, run `mise bootstrap`), bootstrap.sh, .gitignore and five images. The README has three `TODO capture` placeholders and states that the repository stays private until a fresh install is proven and release is approved.

Fresh-install proof passed: Algomarchy task-82 (accepted, 2026-10-16) installed Omarchy in a disposable Quickemu VM, ran the bootstrap and `mise bootstrap`, rebooted and verified the configured desktop. Plan and approvals: Algomarchy task-81 (two repos, setup maintained directly) and task-83 (generated dotfiles made coherent for the bootstrap).

Algorant/Algomarchy stays the PRIVATE operations repository (publisher, private notes); last commit 2026-10-25. The profile still links Algorant/Algomarchy, a dead link for visitors (accepted as motivation).

Conflict: `bootstrap.sh` clones `https://github.com/Algorant/dotfiles.git` by default, and the README links plugin folders and the Omarchy profile in Algorant/dotfiles. Algorant decided on 2026-10-21 that the generated dotfiles stay private (task-12), so a stranger can follow neither.


## Shippable means

The common bar in AGENTS.md, plus: a section per major Omarchy area (e.g. packages, theme and Verdigris, keybindings, terminal and shell, mise bootstrap, agents) that explains what was changed. The generated dotfiles repository stays private (task-12), so the guide cannot rely on links into it.

## Crippling issues

1. The bootstrap and README depend on the private Algorant/dotfiles (see State). Recommended to Algorant via Herdra (2026-10-26): make omarchy-setup self-contained, so the bootstrap takes the reader's own dotfiles source and plugin links become excerpts or screenshots.
2. Three capture placeholders remain in the README.
3. Release not approved; the profile link still points at the private operations repository.


## Next step

Herdra has put the rework question to Algorant (2026-10-26); record his answer. If approved, the Algomarchy Ceph reworks omarchy-setup and fills the captures; then Algorant approves the release and the profile link is repointed to Algorant/omarchy-setup.
