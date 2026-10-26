---
id: task-4
uid: 65bf0b8b-f1b6-45e8-b6eb-028665166e14
type: task
title: "01 — Verdigris: ship publicly"
state: todo
references: ["https://github.com/Algorant/verdigris", "https://github.com/Algorant/omarchy-verdigris-theme"]
tags: ["public-readiness", "verdigris"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:57Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-26T03:53:21Z"
priority: "high"
---
## State

Verdigris now has a public, independently installable Omarchy theme. Verified 2026-10-15: Algorant/omarchy-verdigris-theme is PUBLIC, responds anonymously with HTTP 200, and an anonymous shallow clone succeeds at 911bb6a. Its tree has an MIT LICENSE, five README-linked desktop/app previews, colors.toml, and 28 wallpapers. The README documents `omarchy theme install https://github.com/Algorant/omarchy-verdigris-theme`; it installs as `verdigris`. This check verified public access and contents, not a fresh desktop installation.

Algorant approved publication after a final audit, reported by Herdra on 2026-10-15. The reported audit found no secrets; approved already-public author metadata is not a blocker. This portfolio check did not independently repeat the full-history audit.

Algorant/verdigris remains PRIVATE (visibility rechecked). It holds the canonical palette and other ports; its omarchy/ directory is a stub pointing to the extracted theme (92e417d). The theme retained its history when extracted (verdigris task-1, archived/accepted). The profile still links the private main repository, deliberately retained by Algorant.

## Readiness scan (2026-10-26)

Read-only pattern scan of the current tree and full history of every branch (gitleaks/trufflehog not installed); findings by path or commit, no values. Gmail in commit authorship is approved.

- Main repo: no licence; README.md:39 still "#todo make this a table"; first-name username in Windows paths at obsidian/verdigris-minimal.css:5 and windows-terminal/README.md:16,82, plus 4 history commits; one machine name in history (801b585). Links fine (verdigris.nvim is public). No credentials; no blob over 1 MB.
- Public theme: MIT licence; clean apart from one machine name in history; README.md:37 still carries the private-era install paragraph.

Why private: "keep it private like verdigris for now" (Algorant via Herdra, 2026-10-12); no reason recorded beyond "for now".

## Shippable means

The common bar in AGENTS.md, for each repository, plus:
- the main README shows screenshots of the main ports and links verdigris.nvim;
- the theme installs from its public HTTPS URL with `omarchy theme install`.

## Crippling issues

1. The main repository is still private: the profile link and the theme README's links to its palette and dedicated ports do not resolve anonymously. This does not prevent cloning the public theme.
2. The main repository's previously recorded license, unfinished Ports README and history/attribution checks remain unconfirmed here; the public theme now has its own MIT LICENSE and previews. Do not carry the old theme license/private-access blockers forward.
3. The public theme README still contains private-repository installation guidance; its wording needs refreshing now that anonymous HTTPS cloning works.

## Next step

Herdra has asked the verdigris Ceph (2026-10-26) to finish the Ports table, replace the username paths and drop the theme's stale private paragraph. Questions with Algorant via Herdra: MIT licence for his repos, and publishing the main repo after these fixes, accepting the first name in 4 old commits (both recommended).
