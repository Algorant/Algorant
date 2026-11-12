---
id: task-13
uid: 6f9ff1e9-1bcb-4f15-821a-c46dd8b078b0
type: task
title: "5 — Algomarchy guide: omarchy-setup, private, bring-up depends on the dotfiles mirror"
state: todo
priority: "high"
tags: ["public-readiness", "algomarchy"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: a section-per-area guide; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:52Z"
createdAt: "2026-10-12T01:50:53Z"
updatedAt: "2026-11-12T19:56:44Z"
references: ["https://github.com/Algorant/omarchy-setup", "https://github.com/Algorant/Algomarchy"]
---
## State

`Algorant/omarchy-setup` is the intended public guide (README titled "Algomarchy"); `Algorant/Algomarchy` is the private operations repo. Both private. MIT and gitguard passing (`092fe5b`, 0 findings, 35 commits). Fresh-install proof passed 2026-10-16 on the local-fixture path.

Blocks a stranger today: `bootstrap.sh` defaults to the private (and stale) dotfiles mirror; 7 of 12 referenced images are missing; three `TODO capture` markers; an internal gate sentence about release approval; no banner or one-line licence footer.

## Next step

Algorant decides the name (omarchy-setup stays public, or Algomarchy becomes the guide and the ops repo is renamed), then the owner makes the bring-up self-contained and captures or drops the images.

## Waiting on

The name decision, and the dotfiles card (the guide fetches that mirror).