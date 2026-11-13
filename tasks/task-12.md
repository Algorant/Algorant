---
id: task-12
uid: bf46ebb5-f902-4ebd-9918-22d338256736
type: task
title: "dotfiles: generated mirror, goes public with the guide"
state: "in-progress"
priority: "high"
tags: ["public-readiness", "dotfiles"]
accord:
  status: "blocked"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: Omarchy-era output; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  claimedAt: "2026-11-13T04:40:39Z"
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  note: "Mirror style gap now closed through publisher overlay source 845d01f; workflow 43367773795 succeeded, generated mirror tip 3855b39 (source 129fcbf). Banner title and MIT footer match overlay; second publisher run no-op. Gitguard tip no findings; history no findings in 48 commits, 22 media manually reviewed safe, still tool-unverified (gitguard task-18). Same Sideshow post now shows both README renders and 27-blob combined safe/hold table: http://desktop.tail1cefc.ts.net:8228/session/i3YyIHqkN5M. Still private; awaiting Algorant's look and explicit flip word."
  updatedAt: "2026-11-13T04:48:44Z"
createdAt: "2026-10-12T01:50:52Z"
updatedAt: "2026-11-13T04:48:44Z"
assignee: "algomarchy"
---
## State

`Algorant/dotfiles` is the generated mirror of `.dotfiles@omarchy`: PRIVATE, MIT, reference README note, clean tree, gitguard 0 findings at `940f3a0`.

**Still stale.** The mirror was last synced 2026-10-29 from source `f8cd3f8`; `.dotfiles@omarchy` is now at `129fcbf` (2026-11-12), at least 115 commits further. On 2026-11-09 the tree compare showed 29 upstream files missing with no ignore rule, 8 deleted files still published, and 23 same-path files differing.

## Decided (Algorant, 2026-11-12, via Herdra)

**The dotfiles go public together with the Algomarchy guide.** This reverses the 2026-10-21 "stays private", and the flip itself still needs his explicit word for that repository at that moment.

## Next step

1. One `gh workflow run publish-dotfiles.yml` refresh, then diff the export against `.dotfiles@omarchy` at `129fcbf`.
2. Fix the ignore rules so additions and deletions both flow.
3. Banner and the one-line licence footer in the mirror's README.
4. gitguard re-scan after the refresh.
5. One flip word from him, covering this and the guide.

Owner of the change: the Algomarchy Ceph. The guide card depends on this one.