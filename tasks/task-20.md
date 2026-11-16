---
id: task-20
uid: dc59d85d-f198-46f7-a527-14ad39f29bd5
type: task
title: "GitHub profile README: the front door"
state: todo
priority: "medium"
effort: "small"
accord:
  status: "ready"
  acceptance: ["Every profile link resolves for an anonymous visitor, or is deliberately marked private", "Wording follows repo-style-rules"]
  updatedAt: "2026-11-12T19:56:58Z"
createdAt: "2026-11-12T19:56:58Z"
updatedAt: "2026-11-16T17:11:18Z"
---
The profile README (`README.md` here) is the public front door. Wording and links change under this card.

## State

The existing algomarchy entry still links the old operations repository. Leave it unchanged for now: the replacement showroom is not public yet. The herdra entry stays marked private until Algorant raises it.

## Historical names (Algorant, 2026-11-13, via Herdra)

"lets lock in algomarchy and .algomarchy for now"

`algomarchy` is the public showroom, currently prepared in private `omarchy-setup`, with a fresh-history `Algorant/algomarchy` taking over at the very end before publication. Private ops, installer, VM proof and publisher live in `Algorant/.algomarchy` (standard checkout `~/.algomarchy`); `algomarchy-bootstrap` is folded in and archived.

Earlier 2026-11-12 approval to repoint to `omarchy-setup` is superseded by these names.

## Current identity — landed 2026-11-14

Private `Algorant/.algOS`, checkout `~/.algOS`, owner algOS Ceph. Future public showroom `Algorant/algOS`, a tailored Omarchy/Arch setup, replaces the former proposed public name. Mixed case is explicitly approved.

## Next step

The local README draft now says `[algOS](https://github.com/Algorant/algOS) — My tailored Omarchy/Arch setup. Private for now.` It is a draft, not published. Do not push until the showroom's separate flip approval and anonymous verification of its final public URL. Archived records and historical quotes stay unchanged.

## Done 2026-11-16

The algOS entry links `https://github.com/Algorant/algOS` (commit `e35e982`), verified on the signed-out profile page and the target returns 200. Remaining: herdra stays marked private for now; the "veridgris" link text is a typo of verdigris (link itself works).