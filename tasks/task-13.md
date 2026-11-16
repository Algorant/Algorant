---
id: task-13
uid: 6f9ff1e9-1bcb-4f15-821a-c46dd8b078b0
type: task
title: "algOS: showroom prepared privately, fresh public repo at the end"
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
updatedAt: "2026-11-16T03:49:45Z"
references: ["https://github.com/Algorant/omarchy-setup", "https://github.com/Algorant/.algOS"]
assignee: "algomarchy"
---
## State

The showroom is prepared in private `Algorant/omarchy-setup`, tip `e85bb03` ("Make algomarchy a showroom with app and plugin galleries"), verified on GitHub 2026-11-13. Bring-up and `bootstrap.sh` are removed from HEAD; galleries and source pages are built. The owner's Accord note records gitguard tip/history passes and hand-reviewed media, plus the remaining screenshot concern. The current source history still contains the old installer; it is not the proposed public history.

## Current identity — cutover landed 2026-11-14

Private operations: `Algorant/.algOS`, checkout `~/.algOS`, owner **algOS Ceph**. Future public showroom: `Algorant/algOS`, prepared in private `omarchy-setup` until the final fresh-history handoff. Framing: **a tailored Omarchy/Arch setup**, not an operating system. Mixed case is explicitly approved. dotfiles stays dotfiles.

## Next step

The algOS Ceph finishes the showroom and prepares the final fresh-history public repo. Obtain separate explicit publication permission then. The profile entry is drafted locally as algOS; do not push it until the final public URL passes anonymous verification.

This card records state only. Historical names and exploratory notes below are retained as history, not current instructions.

## Historical naming record

## Names locked (Algorant, 2026-11-13, via Herdra)

"lets lock in algomarchy and .algomarchy for now"

- `Algorant/algomarchy`: public showroom. At the very end a fresh-history repo takes over the work currently in private `omarchy-setup`, before going public.
- `Algorant/.algomarchy`: private operations, installer, VM proof and publisher; standard checkout `~/.algomarchy`.
- `algomarchy-bootstrap` is folded into private operations and archived (GitHub confirms archived).
- Ops checkout is now `~/.algomarchy`, with origin `Algorant/.algomarchy`; its Ceph runs there. `~/Projects/Algomarchy` is gone (verified by Herdra, 2026-11-14).

## Earlier approval, retained as history

Algorant approved keeping `omarchy-setup` as the public name on 2026-11-12. The locked 2026-11-13 names supersede that approval; they do not authorize a visibility flip.

## Next step

The algomarchy Ceph finishes the showroom review and prepares the fresh-history public-name handoff at the end, keeping installer and old source history private. Obtain Algorant's explicit flip word then. After the showroom is public, this workspace repoints the profile to `Algorant/algomarchy` (profile card).

This card records state only. Implementation and acceptance remain with its Ceph.

## Rename alignment under discussion (Algorant, 2026-11-14, via Herdra)

"Ok so my omarchy-setup repo is the one we were going to switch to 'public' algomarchy when ready. We also created art for 'algOS' which I think is what I want to change 'algomarchy' to be. Can we explore what your understanding of that is, and bring both the algorant and algomarchy cephs into it to discuss and make sure everyone is aligned and on the same page?"

Alignment discussion: http://desktop.tail1cefc.ts.net:8228/session/0kP-K1iU0P0 (post "algOS: aligning on the rename"). Candidate public showroom name: algOS instead of algomarchy. Scope, repository casing and private-operations naming are not yet settled. No rename, visibility change, profile edit or replacement of the earlier recorded names is authorized by this exploratory discussion.

## Decided name and scope (Algorant, 2026-11-14, via Herdra)

"for 'algOS' yes this would be a full cutover from anywhere theres 'algomarchy'. so my private repo is .algOS and my public one is Algorant/algOS yes mostly always capitalized for style points. its not actually an operating system, just a tailored omarchy/arch setup"

This supersedes the 2026-11-13 algomarchy/.algomarchy name lock and settles the exploratory alignment above: full cutover, private `.algOS`, public `Algorant/algOS`, with mixed case explicitly approved as an exception to the lowercase style rule. Framing: a tailored omarchy/arch setup, not an operating system.

Implementation has not been declared landed. The owning Ceph plans cutover order; retain current-state names in card titles, other cards and VISION until Herdra confirms the rename has landed. No rename or file change performed here. Naming approval is not permission to flip visibility; that remains separate.

Landed confirmation (Herdra, 2026-11-14): the private rename, checkout move and Ceph cutover above are complete; earlier instructions to wait for that notice are superseded. Publication remains unapproved.

## Milestone — verified 2026-11-16 (read-only, GitHub)

- Showroom README in private `omarchy-setup` is the new 35-line expandable skeleton at `c26d72d` (Algorant: "new readme is better"). Media placeholders wait on Algorant's own captures.
- Installer proven in a fresh VM (fully unattended: one pass, reboot, no-change rerun, per the algOS Ceph via Herdra) and merged privately: `.algOS` master `002a07d` ("Squash commits from native-installer-vm-proof-2").
- Visibility unchanged: `Algorant/.algOS`, `Algorant/omarchy-setup` and `Algorant/dotfiles` all PRIVATE. Flip permission remains separate.

Remaining before the flip: Algorant's captures for the media placeholders, the final fresh-history `Algorant/algOS` handoff, then his explicit flip word for the showroom and dotfiles together.