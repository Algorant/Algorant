---
id: task-7
uid: 139946fd-ffb5-4df1-bd81-18bb8385b10a
type: task
title: "10 — RSSify: prepare for public sharing (not in focus)"
state: todo
references: ["https://github.com/Algorant/rssify"]
tags: ["public-readiness", "rssify"]
accord:
  status: "ready"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope and address the agreed blockers; verify documentation, licensing/attribution, setup and usage claims, and experimental limitations against repository behavior.", "Record applicable repository-native checks and any explicit validation gaps, then record Algorant's approval of the public-facing result or explicit keep-private/defer decision."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:41Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-29T03:47:12Z"
priority: "low"
---
## State

Linked from the profile README but not in the current focus (VISION.md). GitHub: https://github.com/Algorant/rssify. Checkout: ~/Projects/rssify (not present on every machine). Not reviewed since the original inventory.

## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- PUBLIC repository; no licence. Home paths and machine names in AGENTS.md and plan/; committed third-party feed dumps in artifacts/failed-feeds/. No credentials.

Licence decision (Algorant via Herdra, 2026-10-26): MIT, copyright Algorant. RSSify has no local checkout or Ceph, so adding it is parked with Algorant.

Visibility: public.

## Crippling issues

None open. A paid-podcast subscriber feed token was found in the tracked database and OPML exports (2026-10-29). They were untracked in aa2470f. Algorant confirmed the subscription is inactive, so the token is moot: no rotation, no history rewrite, and RSSify stays public. MIT LICENSE added (915b1b9); the third-party failed-feed dumps are untracked.


## Next step

None until Algorant brings it into focus.
