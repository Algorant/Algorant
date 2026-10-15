---
id: task-12
uid: bf46ebb5-f902-4ebd-9918-22d338256736
type: task
title: "04 — Dotfiles: republish from the Omarchy stream"
state: todo
priority: "high"
tags: ["public-readiness", "dotfiles"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md and its own addition: Omarchy-era output; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:52Z"
createdAt: "2026-10-12T01:50:52Z"
updatedAt: "2026-10-15T19:20:21Z"
---
## State

The dotfiles are the `omarchy` branch of private Algorant/.dotfiles (Omarchy machines, `mise bootstrap`). ~/.dotfiles and sysup are retired. The homelab keeps a private, offsite-only branch `archbox` that is never published (cart-lab task-40).

The intended public output Algorant/dotfiles is generated from `.dotfiles@omarchy` by an on-demand publisher in private Algorant/Algomarchy (Algomarchy task-69). It runs only via manual `workflow_dispatch` when Algorant asks or OKs it, uses a fail-closed audit, and has new deploy keys; the old key was rotated. Algomarchy's README, CHECKLIST, and enable-ssh.sh are excluded.

Verified 2026-10-11: Algorant/dotfiles is PRIVATE. Its HEAD is 9613b081 "sync from .dotfiles@omarchy caae0fe22ea2", 214 files, from Algomarchy run 38196500715 (success). The README now describes the Omarchy + mise setup as a reference copy published from a private source, with no sysup mention; no Algomarchy README/CHECKLIST/enable-ssh.sh is in the tree. Algorant is inspecting it. Going public is his call; the profile link 404s until then (accepted).

Update verified 2026-10-15: Algorant/dotfiles remains PRIVATE; its description now reads "My Omarchy setup on Arch Linux, themed Verdigris and reproduced with mise" (the stale sysup description is fixed). Algorant/omarchy-setup is also PRIVATE. Herdra reports that publication of both is gated on the omarchy-setup VM proof; the independently published Verdigris theme does not lift that gate. The 2026-10-11 snapshot above is historical evidence, not a verification of today's complete output. Algorant/.pi remains private and optional, never cloned as part of the setup (Herdra's stated boundary).

Earlier history cleanup: archived task-1 and task-11.

## Shippable means

The common bar in AGENTS.md, plus: the public output and README reflect the Omarchy + `mise bootstrap` setup and point to the Algomarchy guide.

## Crippling issues

1. Publication remains gated on omarchy-setup VM proof and Algorant’s approval; anonymous visitors still cannot follow the profile link.
2. The README does not yet point to an Algomarchy guide (none exists yet; task-13).
3. The new publish was appended on top of the earlier Arch/sysup-era history (parent 25353e5f), which was public before. That history passed the earlier cleanup (task-11), so this is a presentation choice rather than a safety issue: going public exposes the old commits as well.

## Next step

The setup owner supplies the omarchy-setup VM proof through Herdra; Algorant then reviews the private generated output (task-12-1) and decides on publication/history. Do not make dotfiles or omarchy-setup public merely because the Verdigris theme is now public.
