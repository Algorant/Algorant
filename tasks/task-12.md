---
id: task-12
uid: bf46ebb5-f902-4ebd-9918-22d338256736
type: task
title: "dotfiles: generated mirror, goes public with the guide"
state: todo
priority: "high"
tags: ["public-readiness", "dotfiles"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: Omarchy-era output; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:50Z"
createdAt: "2026-10-12T01:50:52Z"
updatedAt: "2026-11-12T20:12:01Z"
---
## State

`Algorant/dotfiles` is the generated mirror of `.dotfiles@omarchy`: MIT, reference README note, clean tree, gitguard 0 findings at `940f3a0`.

The mirror is **115 commits behind** `.dotfiles@omarchy`: 29 upstream files missing with no ignore rule, 8 deleted files still published, 23 same-path files differ. Last publisher run 2026-10-29.

## Decided (Algorant, 2026-11-12, via Herdra)

**Approved: the dotfiles go public together with the Algomarchy guide.** This reverses the 2026-10-21 "stays private" decision, and the flip itself still needs his explicit word for that repository at that moment.

## Next step

1. One `gh workflow run publish-dotfiles.yml` refresh, then diff against `.dotfiles@omarchy`.
2. Fix the ignore rules so additions and deletions both flow.
3. Banner and the one-line licence footer in the mirror's README.
4. gitguard re-scan after the refresh.
5. Ask him for the flip together with the guide, then the visibility change itself.

Owner of the change: the Algomarchy Ceph. The guide card depends on this one.