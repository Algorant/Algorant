---
id: task-12
uid: bf46ebb5-f902-4ebd-9918-22d338256736
type: task
title: "04 — Dotfiles: stays private (Algorant's decision)"
state: todo
priority: "low"
tags: ["public-readiness", "dotfiles"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: Omarchy-era output; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:52Z"
createdAt: "2026-10-12T01:50:52Z"
updatedAt: "2026-10-27T03:12:37Z"
---
## State

Decision (Algorant, reported by Herdra 2026-10-21): the generated Algorant/dotfiles repository stays private. It is not a publication target.

Verified: Algorant/dotfiles is PRIVATE (anonymous request returns 404). GitHub last recorded a change on 2026-10-12. Its description reads "My Omarchy setup on Arch Linux, themed Verdigris and reproduced with mise".

Background: the dotfiles are the `omarchy` branch of private Algorant/.dotfiles, bootstrapped with `mise bootstrap`. An on-demand publisher in private Algorant/Algomarchy (task-69) generates Algorant/dotfiles from it with a fail-closed audit. The homelab server's own branch is offsite-only and never published. Earlier history cleanup: archived task-1 and task-11.

## Shippable means

Not applicable while the decision stands. If Algorant reopens publication: the common bar in AGENTS.md, plus Omarchy-era output and a README that reflects the Omarchy + `mise bootstrap` setup.

## Crippling issues

None. The profile README no longer links Algorant/dotfiles: Herdra chose to remove the "My Dotfiles" entry under its delegation rules (2026-10-21), since it was a dead link for visitors and the Algomarchy entry covers the setup. Removed in 47d69f4, pushed to origin/main.

Work that planned to link public dotfiles files (the Algomarchy guide, task-13) shows the configuration itself instead.

## Next step

None unless Algorant reopens publication.
