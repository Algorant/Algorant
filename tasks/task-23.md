---
id: task-23
uid: 34ca8987-e8b2-4a16-8128-40bd5da5fd07
type: task
title: "Standard License footer across every public and going-public repo"
state: todo
priority: "high"
effort: "small"
relatedFiles: ["VISION.md", "docs/public-readiness.md"]
accord:
  status: "ready"
  acceptance: ["Every public or going-public repo in the table ends its README with exactly '## License' then '[MIT](LICENSE)', verified on GitHub", "Each row is ticked with the commit that landed it", "Rows with no owner were raised to Herdra"]
  updatedAt: "2026-11-17T15:28:39Z"
createdAt: "2026-11-17T15:28:39Z"
updatedAt: "2026-11-17T15:28:39Z"
---

## Description

Algorant (2026-11-17, via Herdra): "only quibble would be at some point we had a 'Licence' section with MIT disclaimer at the bottom, and we did that for my pi setup and one other, but then that format got lost. I want that standardized across all my repos. also my algorant github profile homepage doesn't seem to have the 'use lowercase' treatment, would want that amended. all these things should be tasked and done in parallel."

## The standard (this workspace owns it; in VISION.md and the readiness map, ca16355)

Every README's last section is exactly:

```
## License

[MIT](LICENSE)
```

## Per-repo state (README tails read from GitHub, 2026-11-17)

| Repo | Visibility | State | Owner |
|---|---|---|---|
| tandem | public | ✓ matches | — |
| verdigris | public | ✓ matches | — |
| pi | public | ✓ matches (published catalog) | .pi Ceph (Herdra dispatching a check) |
| algOS | public | ✓ matches | algOS Ceph (dispatched) |
| herdra | private | ✓ matches | herdra manus (dispatched) |
| dotfiles | private | ✗ footer is a bare `[MIT](LICENSE)` after publisher prose, no `## License` heading | algOS Ceph (dispatched) |
| verdigris.nvim | public | ~ `[MIT](./LICENSE)` — same heading, `./` link variant | verdigris Ceph — **not yet dispatched** |
| omarchy-verdigris-theme | public | ✗ no License section (ends on History) | verdigris Ceph — **not yet dispatched** |
| herdr-agent-tree | public | ✗ no License section at the end | Herdra (its plugin) — **not yet dispatched** |
| rssify | public, on the profile | ✗ no License section (ends in a code block) | no Ceph — **not yet dispatched** |
| herdr-notifs-plus | private | ✗ "MIT; see [`LICENSE`](LICENSE)." variant | Herdra — **not yet dispatched** |
| gitguard | private | no LICENSE file on GitHub | gitguard Ceph — only if it goes public |

Out of scope: the GitHub profile README (`Algorant/Algorant`) has no LICENSE file, and forks of other people's repos (e.g. ketch) are not his to restyle.

## How this Task closes

Re-read each README tail on GitHub when its owner reports, tick it here, and complete when every row in scope matches.
