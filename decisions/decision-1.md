---
id: decision-1
uid: ed7e676f-3650-4bd8-8eb2-829a6a361572
type: decision
title: "gitguard covers every public repo, Verdigris included"
status: "proposed"
deciders: ["Algorant"]
createdAt: "2026-11-10T03:27:20Z"
updatedAt: "2026-11-10T03:32:16Z"
---
Algorant, via Herdra 2026-11-09: "Yes: turn gitguard on for Verdigris (and its omarchy theme repo); it's already public." Supersedes his 2026-10-29 decision that "Verdigris stays out until its coexistence design is approved" — for scanning purposes only; the coexistence/readability question is untouched.

Consequence: gitguard covers every public repository, so the checklist row "gitguard passed" applies to Verdigris and Algorant/omarchy-verdigris-theme with no exception.

Done the same day by the Verdigris Ceph (terminal t41):
- verdigris `6aa49f7`: `.gitguard.toml` at the fleet config (enabled, Jev full, offline warn). That clone sets `core.hooksPath=.githooks`, so gitguard is chained into the tracked pre-push guard after Gitleaks on the same stdin, and a tracked `reference-transaction` hook covers board refs.
- omarchy-verdigris-theme `2c9ba58`: `.gitguard.toml` plus `gitguard install`.
- Full-history scans, all refs, 0 unscanned chunks: verdigris 22 commits across 7 refs, theme 13 commits across 3 refs — 0 findings. Wallpaper, swatch and preview images listed as unverified (reviewed by eye).
- Proof the guard fires: a planted secret and a financial-document path were stopped in disposable remotes; clean pushes pass. No accept file, nothing accepted, no history rewritten.

Verified read-only here (2026-11-09): `6aa49f7` present with that `.gitguard.toml`, `core.hooksPath=.githooks`, `.githooks/pre-push` chaining `gitguard hook pre-push` and `reference-transaction` present, and `.gitguard.toml` present on the theme repo's remote.

House method, recorded for the remaining repos: fleet config + chained hook + one planted-push proof.