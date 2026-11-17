---
id: task-26
uid: c59b25ba-f07d-4697-bf51-8f3a486046b7
type: task
title: "herdr-agent-tree: headless demo and README mock (pattern A)"
state: "in-progress"
priority: "high"
effort: "medium"
references: ["https://github.com/Algorant/herdr-agent-tree"]
relatedFiles: ["VISION.md"]
accord:
  status: "claimed"
  acceptance: ["A headless WebP demo of the agent tree exists, made in a scratch hc core via hc-test, with placeholder content only", "A pattern-A README mock (demo after intro, Screenshots section, License footer) is published to Sideshow, and the link reaches Herdra", "Nothing is pushed until Algorant picks; the live core and Herdr window were never touched"]
  claimedAt: "2026-11-17T15:40:17Z"
  updatedAt: "2026-11-17T15:40:17Z"
createdAt: "2026-11-17T15:40:00Z"
updatedAt: "2026-11-17T15:40:17Z"
assignee: "pi:herdr-agent-tree-demo"
---

## Description

Herdra (2026-11-17) assigned herdr-agent-tree's demo to this workspace: its public face is part of the portfolio and it has no other owner. Standard: Algorant's pattern A (task-25, VISION.md): "the demo sells it first".

## Outcome

A looping demo of the agent tree in herdr's sidebar, made headless, plus a README mock in pattern A, shown to Algorant through Herdra. Nothing is pushed until he picks.

## Constraints

- Any hc core used for this is a scratch core driven only through `~/.pi/agent/scripts/hc-test` with `HC_TEST_ROOT` set to its own `/tmp` directory on every call, cleanup included. Never touch the live core, the live Herdr window, Algorant's spaces or focus.
- The demo shows invented placeholder agents and projects only.
- Repo checkout: `~/Projects/herdr-agent-tree` (public, MIT). Edits stay local or on a branch; no push, no release, no visibility change.

## Format

One looping animated WebP (q90, about 10–12 s, sped up, full width) right after the README intro; stills in a `## Screenshots` section near the end, same size, 2-column table, small captions; README ends with `## License` / `[MIT](LICENSE)` (already in place at 073a14e).
