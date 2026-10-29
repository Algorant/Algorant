---
id: task-7
uid: 139946fd-ffb5-4df1-bd81-18bb8385b10a
type: task
title: "11 — RSSify: prepare for public sharing (not in focus)"
state: todo
references: ["https://github.com/Algorant/rssify"]
tags: ["public-readiness", "rssify"]
accord:
  status: "ready"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope and address the agreed blockers; verify documentation, licensing/attribution, setup and usage claims, and experimental limitations against repository behavior.", "Record applicable repository-native checks and any explicit validation gaps, then record Algorant's approval of the public-facing result or explicit keep-private/defer decision."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:41Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-29T03:17:55Z"
priority: "high"
---
## State

Linked from the profile README but not in the current focus (VISION.md). GitHub: https://github.com/Algorant/rssify. Checkout: ~/Projects/rssify (not present on every machine). Not reviewed since the original inventory.

## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- PUBLIC repository; no licence. Home paths and machine names in AGENTS.md and plan/; committed third-party feed dumps in artifacts/failed-feeds/. No credentials.

Licence decision (Algorant via Herdra, 2026-10-26): MIT, copyright Algorant. RSSify has no local checkout or Ceph, so adding it is parked with Algorant.

Visibility: public.

## Crippling issues

1. LEAKED SECRET (found 2026-10-29): a paid podcast subscriber feed token sits in the private feed URL. It appears in the tracked rssify.duckdb (feeds table and about 504 episode enclosure URLs) and in data/PocketCasts.opml:87 and data/PocketCasts_new.opml:94. It has been public in tree and history since about 2026-04-05. Untracked in aa2470f (verified from an anonymous clone: no tracked DB, no OPML files in data/, no token URL in the tree). Deployment runs on the homelab server with its own DB. STILL OPEN: Algorant must rotate the feed URL (asked by Herdra), then the homelab project updates the deployed feed entry. No history rewrite needed once rotated.

MIT LICENSE added (915b1b9). The third-party failed-feed dumps are untracked and gitignored, with history untouched.

## Next step

None until Algorant brings it into focus.
