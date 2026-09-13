---
id: task-1
type: task
title: "01 — Dotfiles: prepare for public sharing"
state: "validation"
priority: "high"
references: ["https://github.com/Algorant/dotfiles", "https://github.com/Algorant/.dotfiles"]
relatedFiles: ["README.md", "docs/public-readiness.md", "docs/dotfiles-verification.md", "docs/task-11-progress.md"]
tags: ["public-readiness", "dotfiles"]
accord:
  status: "delivered"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Replace the README from scratch following Algorant's agreed three-Arch-machine narrative, sysup/tool-ownership explanation, real mise manifest excerpt, bootstrap/profile synchronization description, and linked tool/configuration inventory; do not retain obsolete migration/fallback prose.", "Agree with Algorant on public scope; check documentation, licensing/attribution, setup claims, and live-file/automatic-sync boundaries against actual behavior.", "Address agreed blockers in the authoritative repository and record applicable repository-native checks or explicit validation gaps without modifying this machine's live configuration implicitly.", "Record Algorant's approval of the public-facing result or explicit decision to keep it private/defer; do not publish or change visibility as part of implicit approval."]
  claimedAt: "2026-09-12T04:09:48Z"
  deliveredAt: "2026-09-13T16:18:04Z"
  constraints: ["Do not edit live dotfiles, run bootstrap/sync, push, rewrite history, or change GitHub visibility without explicit authorization.", "Follow the checkout's own instructions and existing Tandem workflow for repository implementation; preserve unrelated work.", "Algorant chose one public dotfiles repository with secrets outside Git, not separate maintained public/private dotfiles repositories. task-11 owns the remediation and verification prerequisite; its completion gates public readiness, not the ability to draft the README."]
  summary: "Dotfiles public-readiness is complete through a privacy-gated generated public repository, and the GitHub profile now points to Algorant/dotfiles."
  evidence: ["Algorant explicitly approved completing this portfolio Task and confirmed the architectural outcome: private Algorant/.dotfiles remains authoritative; public Algorant/dotfiles is generated output.", "GitHub reports Algorant/dotfiles PUBLIC with default branch main; remote HEAD is b61fb063a5e3148ca220fa6687676d2408185ee1.", "The private source workspace's accepted task-35 records 58/58 publication tests, clean actionlint, rejected/corrected/no-op workflow checks, one clean public root commit, and anonymous clone/README verification.", "Five recent Publish public dotfiles workflow runs inspected from the private source repository all completed successfully, including workflow_dispatch and push events.", "README.md now links My Dotfiles to https://github.com/Algorant/dotfiles; docs/public-readiness.md records the generated-source architecture and Pi setup as next.", "No private-source visibility, source-of-truth ownership, or unrelated project content was changed by this portfolio update."]
  filesChanged: ["README.md", "docs/public-readiness.md"]
  updatedAt: "2026-09-13T16:18:04Z"
createdAt: "2026-09-12T03:56:43Z"
updatedAt: "2026-09-13T16:18:04Z"
assignee: "pi"
validation.criterion: "Record Algorant's approval of the public-facing result or explicit decision to keep it private/defer; do not publish or change visibility as part of implicit approval."
validation.note: "Task-11 is complete: README replaced, active history cleaned, fresh-clone checks pass except the reviewed non-credential false positive, and all three main machines are healthy/synchronized. Repository remains private. GitHub's authenticated owner API still resolves an old session-containing commit outside the cleaned refs; no anonymous-access or old-file-content test was performed. Algorant should decide whether to request GitHub Support's retained-object/session-data purge before changing visibility. This is a publication decision, not a secrets-manager implementation task."
validation.requestedAt: "2026-09-12T14:57:46Z"
validation.reviewer: "Algorant"
---
Completed public-readiness outcome. Algorant chose not to expose or retrofit the private `Algorant/.dotfiles` synchronization repository. The private source at `/home/ivan/.dotfiles` now owns the public README source, exclusions, deterministic private replacements, fail-closed audit, tests, and GitHub Action. Its accepted `task-35` produced the separate generated repository `https://github.com/Algorant/dotfiles` with independent clean history.

Verified outcome: `Algorant/dotfiles` is PUBLIC on default branch `main`, currently at `b61fb063a5e3148ca220fa6687676d2408185ee1`. Source task-35 was accepted with 58/58 focused publication tests, clean actionlint, one clean root commit, anonymous README/fresh-clone checks, and successful rejected/corrected/no-op Action behavior. Recent source publication runs continue to complete successfully. The generated repository contains approved public output only; `/home/ivan/.dotfiles` remains the sole source of truth and its own Tandem workspace owns future changes.

Algorant explicitly approved marking this portfolio Task done. The profile README now links My Dotfiles to `https://github.com/Algorant/dotfiles`. Historical investigation notes remain as internal evidence, not the current publication architecture.

Next portfolio repository: task-2, Pi setup at `/home/ivan/.pi`. Follow the workspace rule: inspect local/remote state and the repository's Tandem context, do implementation there, then independently verify and summarize here.