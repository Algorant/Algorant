---
id: task-2
uid: dae194be-bd7a-4d67-9192-1b94ddd630c6
type: task
title: "02 — Pi catalog: polish, then share"
state: todo
references: ["https://github.com/Algorant/pi"]
relatedFiles: ["docs/pi-public-mirror-plan.md", "docs/public-readiness.md", "README.md"]
tags: ["public-readiness", "pi"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:33Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-29T03:49:27Z"
priority: "high"
---
## State

The private source is Algorant/.pi (checkout ~/.pi); last commit 2026-10-22 (43cf1b5). The "Publish Pi snapshot" Action regenerates Algorant/pi on every main push; the latest run succeeded and regenerated the catalog on 2026-10-22 (2128247). Verified 2026-10-26: Algorant/pi is still PRIVATE (top level: README.md, config-manifest.json, extensions, prompts, scripts, skills, themes), so the profile's "My Pi Setup" link 404s (kept on purpose by Algorant as motivation). No public-readiness review of the generated catalog appears on the .pi board.

Recent features: agent inbox, Herdra widget, model roles with quota-aware choice, an adversarial reviewer, dbs, /mem. Codemode is used throughout. Algorant expects a significant codemode-driven refactor, which does not block publishing.


## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- Generated Algorant/pi: no licence; README links the private Algorant/.pi source (dead for visitors); external links resolve. Machine names in docs and code by design (inbox, model roles, memory); a Windows vault path in skills/memory/SKILL.md:30. No credentials; no blob over 1 MB.

Licence decision (Algorant via Herdra, 2026-10-26): MIT, copyright Algorant; sent to the .pi Ceph to add through the publisher.

gitguard pilot phase A (2026-10-28, counts and shapes only; report in the gitguard repo, pilot/history-scan.md): the generated catalog's dbs skill docs and script name the homelab Postgres domain (an internal domain, so a leak; found only by Jev until a literal rule exists); 3 user-home path groups, one a real README example path; machine-name notes. To be fixed in the .pi source before any publication.

gitguard calibration (2026-10-28): the Pi catalog has 4 real findings, including the homelab domain in the dbs docs. These must be fixed in the .pi source before any flip.

Why private: no recorded reason. The public-mirror plan authorized planning only and publication was never approved; the .pi source is private by design.

## Shippable means

The common bar in AGENTS.md, plus: the public README explains the codemode-based tool model wherever it matters, and states the pending refactor as a known limitation.

Algorant keeps the dead profile link on purpose (2026-10-11), as motivation to get this public.

## Crippling issues

None known under the narrowed policy (2026-10-29). The fresh-repo plan (.pi task-491) is cancelled, and the existing private repository and its history stay. gitguard 0.5.0 (ruleset 0.5.0, Jev full, block mode; 2026-10-29) scanned all refs and history (138 commits, tip 22a898f) and reported no findings. The gitguard owner got the same result independently (.pi task-492). The catalog is ready, still private; the flip list is on hold.

## Next step

Reference convention shipped (2026-10-29; verified):
- .pi source e5e152d, catalog 22a898f, publisher run 40811085013 green.
- The README's first line after the title is the exact reference note.
- A publisher-owned AGENTS.md holds only the "Reading this repo as a reference" section.
- Nickname replacements are kept as polish, and the domain stand-in is now example.com.

gitguard 0.4.1 scanned all refs and full history (138 commits): no credential or financial-record findings. When gitguard 0.5.0 releases, the pi Ceph reruns it for personal records (family, address, health, correspondence). Then the flip comes to Algorant as one yes/no. Algorant/pi is still PRIVATE.

Upcoming (Algorant, 2026-10-29; not scoped, nothing started): significant presentability polish first, then sharing through X/Twitter threads, blog posts and videos. Any flip waits for Algorant (the 2026-10-29 flip list is on hold).
