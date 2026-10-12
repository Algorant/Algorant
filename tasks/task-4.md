---
id: task-4
uid: 65bf0b8b-f1b6-45e8-b6eb-028665166e14
type: task
title: "01 — Verdigris: ship publicly"
state: todo
references: ["https://github.com/Algorant/verdigris"]
relatedFiles: ["/home/ivan/Projects/verdigris/README.md"]
tags: ["public-readiness", "verdigris"]
accord:
  status: "ready"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope and address the agreed blockers; verify documentation, licensing/attribution, setup and usage claims, and experimental limitations against repository behavior.", "Record applicable repository-native checks and any explicit validation gaps, then record Algorant's approval of the public-facing result or explicit keep-private/defer decision."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:17Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-12T01:50:17Z"
priority: "high"
---
## State

Algorant/verdigris is PRIVATE, so the profile's Verdigris link is dead for visitors. The repository has a semver palette (css/palette.json, CHANGELOG.md), 14 ports including Omarchy with 5K wallpapers, and logos. Its Tandem board has no active work. It is the project closest to shareable.

## Shippable means

The common bar in AGENTS.md, plus: screenshots of the main ports in the README, and verdigris.nvim linked.

## Crippling issues

1. Private repository, so the profile link 404s.
2. No LICENSE file.
3. The README still has a '#todo make this a table' Ports list, and the Obsidian port is described as an experiment.
4. History not yet checked for private material (exploration files, wallpapers and assets, rights to any third-party bases such as Gruvbox and Everforest attribution).
(Inferred read-only on 2026-10-11; not yet confirmed with the verdigris Ceph.)

## Next step

verdigris Ceph: add a license, finish the README Ports table and screenshots, and review history. Then Algorant decides on making it public.
