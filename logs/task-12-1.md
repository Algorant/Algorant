---
id: task-12-1
uid: c50cc709-5ff7-4c68-be82-c0f6a027eeed
type: task
title: "Deferred: Algorant reviews private Algorant/dotfiles and decides whether it goes public"
priority: "low"
parentId: "task-12"
tags: ["public-readiness", "dotfiles", "deferred"]
accord:
  status: "ready"
  acceptance: ["Algorant has inspected the README, config/, plugins, scripts and rewrites, and any requested changes were republished through the Algomarchy workflow.", "Algorant's history decision (keep or start fresh) is recorded.", "Algorant's visibility decision is recorded, and if he chose public, an anonymous check confirms the repository and the profile link resolve."]
  constraints: ["Visibility changes and history rewrites need Algorant's explicit word.", "Nothing private in this public board."]
  updatedAt: "2026-10-12T03:04:49Z"
createdAt: "2026-10-12T03:04:49Z"
updatedAt: "2026-10-26T01:51:14Z"
archivedAt: "2026-10-26T01:51:14Z"
resolution:
  outcome: "canceled"
  note: "Superseded: Algorant decided Algorant/dotfiles stays private (via Herdra, 2026-10-21). No publication review is pending."
---

## Description

Deferred by Algorant on 2026-10-11, for later. Picks up when Algorant chooses to do the review.

Inspect the private Algorant/dotfiles at the first Omarchy-era publish (9613b081, 214 files). Review these parts listed in the Algomarchy task-69 handoff:
- README.md
- config/
- the Omarchy bar plugins under home/.config/omarchy/plugins/
- the scripts under home/scripts/
- the private-material rewrites the publisher applies (rules in Algomarchy public/replacements.json and public/ignore.txt)

Decide whether to keep the old Arch/sysup-era history under the new publish or start the public repository fresh. Herdra recommends keeping it: it passed the task-11 cleanup and was public before.

Flip it public:
`gh repo edit Algorant/dotfiles --visibility public --accept-visibility-change-consequences`

Republish after changes (the publisher in private Algomarchy is on demand only):
`gh workflow run publish-dotfiles.yml -R Algorant/Algomarchy`

Also before going public: update the stale GitHub description (task-12, crippling issue 1).
