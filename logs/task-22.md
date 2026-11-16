---
id: task-22
uid: 3e22bdc5-43a1-41e4-a254-8a647be27fad
type: task
title: "Review tandem against the readiness bar and correct its card"
priority: "high"
references: ["https://github.com/Algorant/tandem"]
accord:
  status: "ready"
  acceptance: ["The five readiness items (README in repo-style-rules, MIT, gitguard pass at tip, current, mechanism) are each marked met or not met with evidence at the current tip", "README, banner, docs links and install paths (curl, cargo, AUR) are checked against the repo and the live site", "Any gap names its owner; fixes are the tandem Ceph's, not made here", "The board's record of tandem is corrected to the verified state, and one screen reaches Herdra"]
  updatedAt: "2026-11-16T05:31:11Z"
createdAt: "2026-11-16T05:12:43Z"
updatedAt: "2026-11-16T05:31:11Z"
archivedAt: "2026-11-16T05:31:11Z"
resolution:
  outcome: "completed"
  note: "Completed on the tandem Ceph's report (tandem task-114), verified here 2026-11-16:\n- 90ed14e \"Apply the eight approved README and docs tweaks\" is on origin/main; \"Deploy docs site\" succeeded at 90ed14e; trytandem.dev returns 200.\n- Repo PUBLIC, MIT detected; README opens on the light/dark banner (site/public/banner-*.svg).\n- gitguard: pre-push on 2026-11-16 recorded no findings (5 media listed unverified); last full-history pass 0 findings across 1,096 commits at the earlier review tip.\n- Algorant approved all eight tweaks: \"yeah do all 8 go ahead\". Evidence posts: ZCjQb7_I8zY (live after-shots) and 61LDSrUHV1g (review), session http://desktop.tail1cefc.ts.net:8228/session/yf_6Zb7WQVc.\nOpen, not blocking: AUR build (tandem task-104)."
  reviewer: "Algorant"
---

## Description

Algorant (2026-11-15, via Herdra): "so as far as repos to make 'nice' we have tasks to fix dotfiles and herdra, and do a review of tandem, right?"

tandem is public (release 0.17.7, 2026-11-11). Its card (task-3) was completed on 2026-11-12 after the public-face cleanup; this is a fresh review of the repo as it stands, like the verdigris review (task-21).

Owner of the review and any fixes: the tandem Ceph (terminal t1w). This workspace records the result. Not started: Herdra dispatches it once Algorant confirms the order.
