---
id: decision-1
uid: ed7e676f-3650-4bd8-8eb2-829a6a361572
type: decision
title: "gitguard covers every public repo, Verdigris included"
status: "proposed"
deciders: ["Algorant"]
createdAt: "2026-11-10T03:27:20Z"
updatedAt: "2026-11-10T03:27:20Z"
---

Algorant, via Herdra 2026-11-09: "Yes: turn gitguard on for Verdigris (and its omarchy theme repo); it's already public." Supersedes his 2026-10-29 decision that "Verdigris stays out until its coexistence design is approved" — for scanning purposes only.

Consequence: gitguard now covers every public repository, so the five-point checklist row "gitguard passed" applies to Verdigris and Algorant/omarchy-verdigris-theme with no exception. What the old decision was protecting (readability/coexistence of the two palettes) is unaffected and stays a content question, not a scanning one.

Implementation owner: the Verdigris Ceph (terminal t41), asked 2026-11-09 to add `.gitguard.toml` (mode enabled, Jev full, offline warn), install the hooks, and scan tree plus full history at the current tips, reporting categories and paths only. This workspace records the decision; it does not make the change.
