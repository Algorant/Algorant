---
id: task-4
uid: 65bf0b8b-f1b6-45e8-b6eb-028665166e14
type: task
title: "01 — Verdigris: ship publicly"
state: todo
references: ["https://github.com/Algorant/verdigris"]
tags: ["public-readiness", "verdigris"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:57Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-12T13:18:33Z"
priority: "high"
---
## State

Two repositories, both PRIVATE as of 2026-10-11. The profile's Verdigris link is a dead link for visitors (Algorant keeps it on purpose, as motivation).
- Algorant/verdigris: the palette (semver css/palette.json, CHANGELOG.md), its ports, and logos. Its omarchy/ folder is now a stub (92e417d) pointing to the theme repository.
- Algorant/omarchy-verdigris-theme (new, verdigris task-1): the Omarchy port, carved out with its history kept (6 commits). It contains README.md, colors.toml, and two 5K triptych wallpapers, and installs as `verdigris` with `omarchy theme install`. While it is private, install needs the SSH URL. It can go public on its own, ahead of the main repository.

This is still the project closest to shareable.

## Shippable means

The common bar in AGENTS.md, for each repository, plus:
- the README shows screenshots of the main ports and links verdigris.nvim;
- the theme repository installs from its public HTTPS URL with `omarchy theme install`.

## Crippling issues

1. Both repositories are private, so the profile link is dead and the theme cannot be installed by URL.
2. Neither has a LICENSE file. The wallpapers and palette need a stated license.
3. Cross-links: the theme README and the Algomarchy guide link to Algorant/verdigris. If the theme goes public first, those links stay dead until verdigris is public too.
4. The verdigris README still has a '#todo make this a table' Ports list, and its Obsidian port is described as an experiment.
5. History not yet checked in either repository for private material or third-party asset rights (attribution for the Gruvbox and Everforest inspiration).

## Next step

The verdigris Ceph adds licenses to both repositories, finishes the Ports table and screenshots, and checks history. Then Algorant decides on visibility. The theme repository alone can go first if he accepts the dead link back to verdigris.
