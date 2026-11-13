---
id: task-13
uid: 6f9ff1e9-1bcb-4f15-821a-c46dd8b078b0
type: task
title: "algomarchy: showroom prepared privately, fresh public repo at the end"
state: "in-progress"
priority: "high"
tags: ["public-readiness", "algomarchy"]
accord:
  status: "blocked"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: a section-per-area guide; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  claimedAt: "2026-11-13T04:38:51Z"
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  note: "Reframed by Algorant as showroom, not installation guide. Private revision e85bb03 pushed; Bring-up and bootstrap.sh removed from HEAD, tour/demo + plain-English guide placeholders added, app/plugin galleries and source pages completed. Private Algorant/algomarchy-bootstrap tip 3486749 preserves installer-only path history (two original path commits). Gitguard showroom tip no findings with 9 hand-reviewed PNGs tool-unverified; history no findings/45 commits with 14 PNG unverified. New post UpQhXLKkyxM in session http://desktop.tail1cefc.ts.net:8228/session/i3YyIHqkN5M. BEFORE FLIP: old installer/Bring-up still reachable in source history; propose keep old repo private as archive and fresh-history showroom under public name, only with explicit approval. Also cleaner herdr screenshot preferred because supplied crop retains release chatter and local URL. No source history rewrite, rename or visibility change."
  updatedAt: "2026-11-13T05:15:22Z"
createdAt: "2026-10-12T01:50:53Z"
updatedAt: "2026-11-13T16:41:46Z"
references: ["https://github.com/Algorant/omarchy-setup", "https://github.com/Algorant/.algomarchy"]
assignee: "algomarchy"
---
## State

The showroom is prepared in private `Algorant/omarchy-setup`, tip `e85bb03` ("Make algomarchy a showroom with app and plugin galleries"), verified on GitHub 2026-11-13. Bring-up and `bootstrap.sh` are removed from HEAD; galleries and source pages are built. The owner's Accord note records gitguard tip/history passes and hand-reviewed media, plus the remaining screenshot concern. The current source history still contains the old installer; it is not the proposed public history.

## Names locked (Algorant, 2026-11-13, via Herdra)

"lets lock in algomarchy and .algomarchy for now"

- `Algorant/algomarchy`: public showroom. At the very end a fresh-history repo takes over the work currently in private `omarchy-setup`, before going public.
- `Algorant/.algomarchy`: private operations, installer, VM proof and publisher; standard checkout `~/.algomarchy`.
- `algomarchy-bootstrap` is folded into private operations and archived (GitHub confirms archived).
- On this machine the ops checkout is still `~/Projects/Algomarchy`, with origin already `Algorant/.algomarchy`; the standard location is not present locally. Moving it belongs to its owner.

## Earlier approval, retained as history

Algorant approved keeping `omarchy-setup` as the public name on 2026-11-12. The locked 2026-11-13 names supersede that approval; they do not authorize a visibility flip.

## Next step

The algomarchy Ceph finishes the showroom review and prepares the fresh-history public-name handoff at the end, keeping installer and old source history private. Obtain Algorant's explicit flip word then. After the showroom is public, this workspace repoints the profile to `Algorant/algomarchy` (profile card).

This card records state only. Implementation and acceptance remain with its Ceph.