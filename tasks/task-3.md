---
id: task-3
uid: 4f6c1fe0-535e-402c-9cf1-eca0d9988dd6
type: task
title: "01 — Tandem: polish, then share"
state: todo
references: ["https://github.com/Algorant/tandem"]
tags: ["public-readiness", "tandem"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:35Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-11-11T17:01:13Z"
priority: "high"
---
## State

Algorant/tandem is PUBLIC, at 0.17.5 (tag `tandem-v0.17.5`, 2026-11-08), MIT. Verified 2026-11-09: the docs site at trytandem.dev returns 200 and is generated from `docs/` (Astro Starlight in `site/`, synced by `site/scripts/sync-docs.mjs`), the release carries 13 assets including the installer and linux/darwin x86_64+aarch64 tarballs, AUR `tandem-bin` is 0.17.5-1, and every command in `tandem --help` appears in the CLI docs with no name mismatches. gitguard is enabled (fleet config) and passed at `121aee5`: 1054 commits, 65 refs, 0 findings.

Public-reader first impression today: an empty About (no description, homepage or topics), 0 open issues with no issue template, and the README is 53 lines with no screenshot, no status line and no report path.

## Shippable means

The common bar in AGENTS.md, plus: the site and README carry the current brand, and the docs match current behavior.

## Crippling issues

1. The public `tandem` branch is the internal work log: 156 files and 381 commits of task/decision/log/event records naming machines, coordinator message ids and private project names, plus `plan/` research directories and an AGENTS.md describing the private workflow. Under the narrowed framework this is not a privacy violation, but it is one click from the README and the opposite of straightforward.
2. README: no status statement (pre-1.0, protocol 0.5.0), no screenshot or teaser, no known issues, no link to the 45-section `RELEASES.md`, no way to report a problem, no AUR mention.
3. Repo About metadata empty; Issues open but no template, Discussions off.
4. Stale docs lines: the CLI page still says "move every machine to 0.17.1" and another page pins 0.17.3; `extensions/` is an empty "future" placeholder.
5. Minor: `.gitguard.toml` cites a personal notes document; the Brainfile attribution question in AGENTS.md is unresolved.

## Next step

Algorant started the public-repo review on 2026-11-09: the tandem Ceph is reviewing README, cleanup and banner against its repo-style-rules, with a gitguard scan alongside, and its proposals land in the Sideshow session "Public repos: tandem". Since tandem is already public, this is cleanup, simplification and look rather than a visibility flip.

This workspace records state only. My six-repo plan post carries the tandem section (README, About, board-branch decision, doc lines) and the proposals addressed to the tandem board: http://desktop.tail1cefc.ts.net:8228/session/RcUrkMsFz1A

Upcoming (Algorant, 2026-10-29; not scoped): presentability first, then sharing through X/Twitter threads, blog posts and videos.