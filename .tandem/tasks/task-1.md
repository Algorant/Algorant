---
id: task-1
type: task
title: "01 — Dotfiles: prepare for public sharing"
state: "in-progress"
priority: "high"
references: ["https://github.com/Algorant/.dotfiles"]
relatedFiles: ["/home/ivan/.dotfiles/README.md", "docs/public-readiness.md"]
tags: ["public-readiness", "dotfiles"]
accord:
  status: "claimed"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope; check documentation, licensing/attribution, setup claims, and live-file/automatic-sync boundaries against actual behavior.", "Address agreed blockers in the authoritative repository and record applicable repository-native checks or explicit validation gaps without modifying this machine's live configuration implicitly.", "Record Algorant's approval of the public-facing result or explicit decision to keep it private/defer; do not publish or change visibility as part of implicit approval."]
  claimedAt: "2026-09-12T04:09:48Z"
  constraints: ["Do not edit live dotfiles, run bootstrap/sync, push, rewrite history, or change GitHub visibility without explicit authorization.", "Follow the checkout's own instructions and existing Tandem workflow for repository implementation; preserve unrelated work."]
  updatedAt: "2026-09-12T04:09:48Z"
createdAt: "2026-09-12T03:56:43Z"
updatedAt: "2026-09-12T04:09:48Z"
assignee: "pi"
---

## Description

First repository, explicitly prioritized by Algorant ahead of README order. GitHub: https://github.com/Algorant/.dotfiles (currently private). Authoritative checkout: /home/ivan/.dotfiles; origin verified. Personal configuration and mise-managed live-file history. README describes automatic history publishing and distinguishes live files from checkout-owned artifacts: review that ownership model and repository-local instructions before any changes. Conduct the review with Algorant; capture concrete remediation after findings, not speculative rewrites. This is a coordination Task, not authority to run setup or change live configuration.
