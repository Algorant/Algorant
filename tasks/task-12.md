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
updatedAt: "2026-11-13T16:41:46Z"
assignee: "algomarchy"
---
## State

`Algorant/dotfiles` is the PRIVATE generated mirror of `.dotfiles@omarchy`. The stale snapshot has been refreshed: GitHub tip `3855b39` says "sync from .dotfiles@omarchy 129fcbfb8b30" (verified 2026-11-13). The owner's Accord note records workflow 43367773795 successful, the second run a no-op, README banner and MIT footer matched, gitguard history clean across 48 commits, and 22 media manually reviewed (tool-unverified).

## Approved direction

Algorant approved public dotfiles together with the showroom on 2026-11-12, reversing the earlier private-only direction. Obtain explicit permission for the actual flip at that moment.

## Naming update (Algorant, 2026-11-13)

The publisher and its private operations now belong to `Algorant/.algomarchy`, standard checkout `~/.algomarchy`. `algomarchy` is the public showroom, prepared in private `omarchy-setup` until a fresh-history handoff at the end. `algomarchy-bootstrap` is folded into private ops and archived. This supersedes current-state references to the old `Algorant/Algomarchy` name, not the archived history.

## Next step

Await Algorant's review and explicit flip word alongside the showroom. The refresh and README-style gap are closed. Owner: the algomarchy Ceph; this card records state only.