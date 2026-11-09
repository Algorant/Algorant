---
id: task-18
uid: dd82eec9-33f1-44a4-84c3-bde894645683
type: task
title: "Migration plan for six public repos (pi, dotfiles, Algomarchy, tandem, verdigris, herdra)"
state: "in-progress"
priority: "high"
effort: "large"
accord:
  status: "claimed"
  acceptance: ["One Sideshow post published covering all six repos in Algorant's order, each with public state, blockers, simplify/rescope items, shortest path, and the five-point readiness checklist marked met/missing/unknown with evidence", "Board-level rescope proposals named per project as suggestions for each owner, not applied", "Cross-repo themes and a proposed order of work included", "No public flip, push or other-repo edit made"]
  claimedAt: "2026-11-09T22:04:55Z"
  updatedAt: "2026-11-09T22:04:55Z"
createdAt: "2026-11-09T22:04:46Z"
updatedAt: "2026-11-09T22:04:55Z"
assignee: "algorant"
---

## Description

## Algorant's words (verbatim)

"I want to reopen Algorant and, in light of all the recent changes, get an idea of how we migrate all the things we are working on. a few tasks can be simplified, and a few things can be rescoped, at the intersection of me wanting to make my repos public starting with 1) pi setup 2) dotfiles setup 3) Algomarchy guide 4) tandem 5) verdigris 6)herdra. some of these are already public and some are planned to be public but I mean seeing and reorganizing around what I can do to make them all simple, straightforward, public, and ready to go"

## "Ready to go public" definition (Algorant, via Herdra 2026-11-09, verbatim)

"that means organized nice readme, licence (always generic MIT no fuss), gitguard approved/passed, and having the latest updtaes along with confirming that private -> public actions work appropriately and consistently"

Per-repo checklist, marked met / missing / unknown with evidence:
1. Organized, readable README.
2. Licence: plain MIT, no deliberation.
3. gitguard scanned it and passed (gitguard has its own Ceph; ask through Herdra for scans).
4. Current with the latest changes, not a stale snapshot.
5. Private→public mechanism (visibility flip, or generated public mirror such as the dotfiles) verified correct and repeatable.

## Deliverable

One Sideshow post: a plan, not changes. Per repo, in his order: current state + blockers, simplify/rescope items (Tasks to close/merge/reword — proposed to owners), shortest path, and the five-point checklist matrix. Then cross-repo themes (shared README style, secrets hygiene) and a proposed order of work.

## Boundaries

Other projects' boards and files belong to their Cephs: read freely, propose for owners. Nothing flips to public without Algorant's explicit OK at that moment. Questions go to Herdra.

## Leads from Herdra (verify read-only)

- .pi: skills consolidated (utils, herdr, tandem+triage, studio); pi-slash-prompts and pi-shell retired; pi-agency metrics removed (~-7.6k lines); low-value tools removed; pi-ui trimmed; compact footer; browse sign-in by reference to Proton Pass; secrets rules reworded; reload-freeze fix; model cutover to DeepSeek V4.1 Flash via OpenCode Go. Skills test-and-trim proposal awaits his decision (.pi task-627).
- Herdra: notification filtering, widget layout, cutover script; board still carries stale worktop items.
- Dotfiles + Algomarchy guide owned by Algomarchy (public dotfiles generated from private omarchy branch on demand).
- Tandem and Verdigris have their own Cephs.
