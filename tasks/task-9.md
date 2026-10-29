---
id: task-9
uid: 4f1d3867-c431-4fd9-b300-737673aa6e7f
type: task
title: "07 — mediafetch: prepare for public sharing (later)"
state: todo
references: ["https://github.com/Algorant/mediafetch"]
tags: ["public-readiness", "mediafetch"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:45Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-29T03:13:45Z"
priority: "low"
---
## State

Algorant/mediafetch remains PRIVATE. Verified 2026-10-29: latest prerelease is **0.1.5** (2026-10-27), BRAT-ready. Its board shows task-46 (native acceptance of the verified candidate) archived as completed with Algorant as reviewer.

Goal: a portable Obsidian media-note plugin across eight media types with narrowed providers, verified outside Obsidian (workbench, Obscura) before Algorant's native check.


## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- MIT licence. Real tailnet name in test/gateway.test.ts:1249-1255 and 5 commits; LAN IP and home paths in old board history. Other hits were false positives ("diagnosis" wording; dependency emails in package-lock.json; .npmrc holds only fund/audit flags). No credentials; no blob over 1 MB.

Why private: no recorded reason (the board's decisions cover private/local use of provider data, not repository visibility).

## Shippable means

The common bar in AGENTS.md, plus: installable through BRAT from the public repository, with an honest provider/credential matrix. A replacement candidate must pass the project's current release gates, outside-Obsidian workflow checks and content-preservation checks, then targeted native acceptance on the workstation. Harness success alone does not prove native Obsidian behavior, mobile support or accessibility.

## Crippling issues

1. Algorant's own trial of 0.1.5 in MasterVault is still outstanding (the mediafetch Ceph has the steps).
2. README and provider/credential guidance must match the verified build before any public claims are refreshed.
3. A real tailnet name in test/gateway.test.ts (the fix was requested from the mediafetch Ceph on 2026-10-26).


## Next step

Algorant runs his 0.1.5 trial in MasterVault. The mediafetch Ceph fixes the test host and refreshes the README. Any flip needs his explicit OK at that moment, plus gitguard verification.
