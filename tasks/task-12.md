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
updatedAt: "2026-10-12T02:37:21Z"
---
## State

Decided 2026-10-11 (Algorant via Herdra):
- The dotfiles are the `omarchy` branch of private Algorant/.dotfiles (Omarchy machines, `mise bootstrap` direction). ~/.dotfiles and sysup are retired. The homelab keeps a private, offsite-only branch `archbox` that is never published (cart-lab task-40).
- The public Algorant/dotfiles will be regenerated from `.dotfiles@omarchy` by a new publisher in private Algorant/Algomarchy (Algomarchy task-69, in progress). It runs on demand only (manual `workflow_dispatch`, after significant changes when Algorant asks or OKs it), with a fail-closed audit, new deploy keys, and the old key rotated. The old `master`-triggered "Publish public dotfiles" workflow is superseded.
- Algomarchy's README, CHECKLIST, and enable-ssh.sh are excluded from the public output.
- Algorant/dotfiles goes private so Algorant can inspect the Omarchy-era content without risk. It goes public again on his call, and its profile link 404s until then (accepted, like Verdigris and Pi). On 2026-10-11 it was still PUBLIC with the old Arch/sysup content; the switch to private is pending.

Earlier history cleanup: archived task-1 and task-11.

## Shippable means

The common bar in AGENTS.md, plus: the public output and README reflect the Omarchy + `mise bootstrap` setup and point to the Algomarchy guide.

## Crippling issues

1. The public content is stale (the retired Arch/Niri/sysup setup) until the first run of the new publisher.
2. The new publisher's audit and exclusions are not yet proven on Omarchy-era content (`home@omarchy/`, `config@omarchy/`, `~/scripts`).

## Next step

The Algomarchy Ceph finishes task-69 and the repository goes private. Then Algorant inspects the generated output and decides when it goes public. Verify the visibility and output here when Herdra reports.
