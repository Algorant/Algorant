---
id: task-10
type: task
title: "10 — AlgoPDF: prepare for public sharing"
state: todo
references: ["https://github.com/Algorant/AlgoPDF"]
relatedFiles: ["/home/ivan/Projects/AlgoPDF/README.md"]
tags: ["public-readiness", "algopdf"]
accord:
  status: "ready"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Agree with Algorant on public scope and address the agreed blockers; verify documentation, licensing/attribution, setup and usage claims, and experimental limitations against repository behavior.", "Record applicable repository-native checks and any explicit validation gaps, then record Algorant's approval of the public-facing result or explicit keep-private/defer decision."]
  constraints: ["Do not push, change GitHub visibility, rewrite history, deploy, bootstrap, or modify live configuration without explicit authorization.", "Preserve unrelated work and use the referenced repository's own instructions, Tandem workflow, and validation commands for implementation."]
  updatedAt: "2026-09-12T03:58:08Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-09-12T03:58:08Z"
---

## Description

Review position 10, following dotfiles first and then README order as agreed with Algorant. GitHub: https://github.com/Algorant/AlgoPDF (visibility at inventory: private). Authoritative checkout: /home/ivan/Projects/AlgoPDF; origin verified. The profile README describes the intended public presentation. Use the common rubric in docs/public-readiness.md, conduct the review with Algorant, and agree on concrete remediation after findings. This Task coordinates the outcome; implementation belongs in the referenced repository under its own instructions. Pre-existing local changes were observed in tsconfig.json and .tandem; preserve them. Check NightPDF attribution and derivative licensing as part of the review.
