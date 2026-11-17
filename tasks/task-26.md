---
id: task-26
uid: c59b25ba-f07d-4697-bf51-8f3a486046b7
type: task
title: "herdr-agent-tree: headless demo and README mock (pattern A)"
state: "todo"
priority: "high"
effort: "medium"
references: ["https://github.com/Algorant/herdr-agent-tree"]
relatedFiles: ["VISION.md"]
accord:
  status: "ready"
  acceptance: ["A headless WebP demo of the agent tree exists, made in a scratch hc core via hc-test, with placeholder content only", "A pattern-A README mock (demo after intro, Screenshots section, License footer) is published to Sideshow, and the link reaches Herdra", "Nothing is pushed until Algorant picks; the live core and Herdr window were never touched"]
  claimedAt: "2026-11-17T15:40:17Z"
  deliveredAt: "2026-11-17T16:06:47Z"
  summary: "Headless looping WebP demo (q90, ~11 s, 3.2x) and 4 same-size stills of the agent tree, placeholder projects only, recorded inside a scratch hc core via hc-test; README pattern-A mock committed on local branch readme-demo (7ca4e99) in ~/Projects/herdr-agent-tree, not pushed; published to Sideshow session s4WydGlg_cA for Algorant's pick."
  evidence: ["Recording ran via HC_TEST_ROOT=/tmp/hat-demo/hc hc-test run (scratch core), stopped with hc-test server stop; no live core, Herdr window, space, tab or focus touched (only this manus's own tab was renamed, as directed)", "Sidebar: isolated Herdr 0.9.5 server (latest release, downloaded into /tmp only; the old herdr TUI is not installed here) with the plugin linked from the checkout; 9 real credential-free Pi sessions on a 127.0.0.1-only scripted model; no provider reached", "readme-demo 7ca4e99: README.md +9 lines (demo after intro, ## Screenshots 2-column table before ## License), images/shots/demo.webp (930 KB) + tree/native/worker/project.png (1280x760)", "scripts/check.sh --no-e2e: All checks passed; PATH=<herdr 0.9.5>:$PATH tests/e2e/sidebar.sh: End-to-end sidebar test passed", "gitguard scan --range 073a14e..readme-demo: no findings in text; 5 media files not scannable, checked by eye (placeholder names only)", "Sideshow: http://localhost:8228/session/s4WydGlg_cA and http://desktop.tail1cefc.ts.net:8228/session/s4WydGlg_cA (MagicDNS HTTP 200)", "Cleanup: /tmp/hat-demo (scratch core, isolated server, Herdr binary, scripts) deleted; no leftover processes; checkout back on main, branch kept"]
  filesChanged: ["~/Projects/herdr-agent-tree: README.md, images/shots/demo.webp, images/shots/tree.png, images/shots/native.png, images/shots/worker.png, images/shots/project.png (branch readme-demo)"]
  note: "discarded: Algorant (2026-11-17): \"herdr-agent-tree is not relevant anymore. I don't think we even use this\". Archive the retired plugin and drop its unpublished demo, not integrate it. Shared portfolio checkout and sessions preserved; separate local demo branch will be backed up and discarded."
  updatedAt: "2026-11-17T19:52:02Z"
createdAt: "2026-11-17T15:40:00Z"
updatedAt: "2026-11-17T19:52:02Z"
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
