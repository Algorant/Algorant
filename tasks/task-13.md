---
id: task-13
uid: 6f9ff1e9-1bcb-4f15-821a-c46dd8b078b0
type: task
title: "Algomarchy guide: omarchy-setup stays the public repo"
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
updatedAt: "2026-11-13T05:15:22Z"
references: ["https://github.com/Algorant/omarchy-setup", "https://github.com/Algorant/Algomarchy"]
assignee: "algomarchy"
---
## State

`Algorant/omarchy-setup` is the intended public guide (README titled "Algomarchy"); `Algorant/Algomarchy` is the private operations repo. Both private. MIT and gitguard passing (`092fe5b`, 0 findings, 35 commits). Fresh-install proof passed 2026-10-16 on the local-fixture path.

Blocks a stranger today: `bootstrap.sh` defaults to the private (and stale) dotfiles mirror; 7 of 12 referenced images are missing; three `TODO capture` markers; an internal gate sentence about release approval; no banner or one-line licence footer.

## Decided (Algorant, 2026-11-12, via Herdra)

**`omarchy-setup` stays the guide's public repository**, the operations repo stays private, and the profile link is repointed to the guide. No rename.

## Next step

1. Make the bring-up self-contained: `bootstrap.sh` takes the reader's own dotfiles URL, with his published mirror as the example.
2. Capture or drop the seven images; remove the internal gate sentence.
3. Banner and one-line licence footer.
4. Ask him for the flip, together with the dotfiles mirror.

## Waiting on

The dotfiles card (the guide fetches that mirror). Owner of the change: the Algomarchy Ceph.