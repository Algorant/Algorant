---
id: task-12
uid: bf46ebb5-f902-4ebd-9918-22d338256736
type: task
title: "dotfiles: private; README rewrite underway"
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
updatedAt: "2026-11-17T00:19:15Z"
assignee: "algomarchy"
---
## State

`Algorant/dotfiles` is the PRIVATE generated mirror of `.dotfiles@omarchy`. The stale snapshot has been refreshed: GitHub tip `3855b39` says "sync from .dotfiles@omarchy 129fcbfb8b30" (verified 2026-11-13). The owner's Accord note records workflow 43367773795 successful, the second run a no-op, README banner and MIT footer matched, gitguard history clean across 48 commits, and 22 media manually reviewed (tool-unverified).

## Approved direction

Algorant approved public dotfiles together with the showroom on 2026-11-12, reversing the earlier private-only direction. Obtain explicit permission for the actual flip at that moment.

## Historical naming update (Algorant, 2026-11-13)

The publisher and its private operations now belong to `Algorant/.algomarchy`, standard checkout `~/.algomarchy`. `algomarchy` is the public showroom, prepared in private `omarchy-setup` until a fresh-history handoff at the end. `algomarchy-bootstrap` is folded into private ops and archived. This supersedes current-state references to the old `Algorant/Algomarchy` name, not the archived history.

## Next step

Await Algorant's review and explicit flip word alongside the showroom. The refresh and README-style gap are closed. Owner: the algOS Ceph; this card records state only.

## Current identity — landed 2026-11-14

Publisher and private operations: `Algorant/.algOS`, checkout `~/.algOS`, owner algOS Ceph. The paired showroom launches as `Algorant/algOS` (fresh history at the end), framed as a tailored Omarchy/Arch setup. This supersedes the older current-name description above. dotfiles stays dotfiles; flip permission remains separate.

## Kept private (Algorant, via Herdra, 2026-11-15)

"leave dotfiles private. the links can just be dead for now"

dotfiles stays private when the algOS showroom flips; links to it may be dead for now. Still pending — this supersedes the "goes public together with the showroom" pairing for the time being. Also raised by him as a repo to fix: "so as far as repos to make 'nice' we have tasks to fix dotfiles and herdra, and do a review of tandem, right?"

## Not ready: README rewrite owed, comes last (Algorant, 2026-11-16, via Herdra)

*"dotfiles doesn't have readiness in the sense that it matters. so far we have done a complete review and overhaul of the readme for every single repo, and this one would be no different. it doesn't have any security issues, which is completely differnet and just one more thing to check off. but that isn't the encapsulation of 'readiness'. skip dotfiles we will come back to it because its obviously going to take the longest once you take into accoutn a readme rewrite"*

The clean gitguard scan and refreshed mirror are one item checked off, not readiness. A full README review and overhaul with Algorant is still owed, as every other repo got, and dotfiles is deliberately the last repo in the sequence because that rewrite will take the longest. Skipped for now; not started.

## README spec and rewrite started (Algorant, 2026-11-16, via Herdra)

"for dotfiles: readme should just cover, how it works at a high level (using mise dot) a quick diagram or sample from mise docs how it hooks in, and then some of the things it keeps track of, at a high levle. if someone is interested they can click into it."

So the README covers three things only: how it works at a high level (mise dot), one quick diagram or mise-docs sample of how it hooks in, and a high-level list of what it tracks, linking into the tree for detail.

The rewrite is underway with the algOS Ceph's manus "Dotfiles README mockup". Still private; the flip needs his separate word. This card records state only.