---
id: task-4
uid: 65bf0b8b-f1b6-45e8-b6eb-028665166e14
type: task
title: "verdigris: public colour scheme repo (rescoping with its Ceph)"
state: todo
references: ["https://github.com/Algorant/verdigris", "https://github.com/Algorant/omarchy-verdigris-theme", "https://github.com/Algorant/verdigris.nvim"]
tags: ["public-readiness", "verdigris"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:37Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-11-13T04:33:39Z"
priority: "high"
---
## State

Both repositories are public: `Algorant/verdigris` (fresh history since 2026-10-26) and `Algorant/omarchy-verdigris-theme` (2026-10-15), MIT, gitguard passing (`6aa49f7` with 22 commits; `2c9ba58` with 13; 0 findings). Old history stays private in `verdigris-archive`.

**Goal (Algorant's words, 2026-11-12):** a public colour scheme repo where people can see what he uses for config, with pictures and demos of what it looks like for every piece of software — modelled on kepano's flexoki: a palette, a real theme file, and a screenshot per supported app.

## In progress

Its Ceph is **actively building the rescope** — commits on 2026-11-12 (`5d3ed95` ANSI slot 7, `55ad1e7` Hyprland borders from the generated theme) after the gitguard adoption. Plan in Sideshow "verdigris rescope".

## Waiting on

Nothing from Algorant. This card records state; content decisions are its Ceph's.