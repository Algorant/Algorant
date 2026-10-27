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
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:51:01Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-27T03:12:36Z"
priority: "low"
---
## State

Algorant/mediafetch remains PRIVATE and unaccepted. Verified 2026-10-26: last commit 2026-10-22 (2bebd20); prerelease **0.1.4** published 2026-10-21 (the previous was 0.1.3, 2026-09-29).

On its board: the diagnosis/repair loop (task-47) is closed, the vault-integration specification (task-3) is parked by Algorant (2026-10-16), and task-46, final native acceptance of the verified candidate in MasterVault on the workstation, is blocked waiting on Algorant's install, credential selection and short native check. task-46 says the parked integration spec is not a prerequisite. This record does not independently confirm that 0.1.4 is the candidate that passed the workbench gates; the mediafetch Ceph should confirm.

Goal: a portable Obsidian media-note plugin across eight media types with narrowed providers, verified outside Obsidian (workbench, Obscura) before Algorant's native check.


## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- MIT licence. Real tailnet name in test/gateway.test.ts:1249-1255 and 5 commits; LAN IP and home paths in old board history. Other hits were false positives ("diagnosis" wording; dependency emails in package-lock.json; .npmrc holds only fund/audit flags). No credentials; no blob over 1 MB.

Why private: no recorded reason (the board's decisions cover private/local use of provider data, not repository visibility).

## Shippable means

The common bar in AGENTS.md, plus: installable through BRAT from the public repository, with an honest provider/credential matrix. A replacement candidate must pass the project's current release gates, outside-Obsidian workflow checks and content-preservation checks, then targeted native acceptance on the workstation. Harness success alone does not prove native Obsidian behavior, mobile support or accessibility.

## Crippling issues

1. No native acceptance yet (task-46 waits on Algorant). Until then, 0.1.4 is an unaccepted prerelease.
2. README and provider/credential guidance must match the verified build before public claims are refreshed.


## Next step

Herdra has asked the mediafetch Ceph (2026-10-26) to replace the real tailnet name in its test with a synthetic host. Task-46 native acceptance is with Algorant. After acceptance, the Ceph refreshes the README and provider matrix; publication still needs Algorant's explicit approval.
