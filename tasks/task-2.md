---
id: task-2
uid: dae194be-bd7a-4d67-9192-1b94ddd630c6
type: task
title: "02 — Pi setup: prepare for public sharing"
state: todo
references: ["https://github.com/Algorant/pi"]
relatedFiles: ["docs/pi-public-mirror-plan.md", "docs/public-readiness.md", "README.md", "/home/ivan/.pi/README.md", "/home/ivan/.pi/.tandem/tasks/task-182.md"]
tags: ["public-readiness", "pi"]
accord:
  status: "ready"
  acceptance: ["Record the approved public-resource scope and migration touchpoints; exclude private/runtime paths without inspecting their contents or auditing private history, and review selected public material plus generated output/history without exposing sensitive values.", "Implement and verify the approved private Algorant/.pi source and generated Algorant/pi architecture in the authoritative ~/.pi workspace, preserving private history and unrelated local work; obtain explicit approval before remote cutover, publication, or live changes.", "Verify public documentation, licensing/attribution, reusable configuration and usage claims against generated output; record Pi-native publication checks and explicit validation gaps.", "After implementation is accepted in Pi's own workspace, independently verify local and remote outcomes, update the portfolio documentation, and record Algorant's approval before completing this coordination Task."]
  constraints: ["Do not push, change GitHub visibility, rewrite history, deploy, bootstrap, or modify live configuration without explicit authorization.", "Preserve unrelated work and use the referenced repository's own instructions, Tandem workflow, and validation commands for implementation."]
  updatedAt: "2026-09-14T01:48:11Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-09-14T03:13:29Z"
---
Algorant decided to use a private authoritative source plus generated public showcase, without a further architecture assessment. Rename the existing private Algorant/pi repository to Algorant/.pi, retain ~/.pi as the authoritative local checkout, and create a replacement Algorant/pi containing sanitized output with independent clean history. Publication rules and automation belong in the private source; the public output is not maintained separately.

High-level sequence and boundaries: docs/pi-public-mirror-plan.md. Algorant requested the implementation handoff: task-182 (Prepare private .pi source and generated public Pi showcase) now exists in /home/ivan/.pi's Tandem workspace. It owns the full outcome with an explicit scoped-plan checkpoint before edits; bounded implementation Tasks or milestones follow there. This hub owns independent final verification. Dotfiles' current publisher is a reference, not an instruction to reuse its destructive recreation helper.

Scope is selected public resources and migration touchpoints. Exclude conversations, sessions, memories, coordination records, credentials and other private/runtime state by path without inspecting their contents or auditing private history. Review selected public content and generated output/history for publication safety and usability. This intentionally narrows the generic review rubric. Follow Pi's current direct-verification/temporary-check rules; no default broad-suite runs or permanent test harnesses.

Initial planning verification: ~/.pi main and remote HEAD matched 5c8826976f758c3c3b618327d0334ee4078c2e56; Algorant/pi was PRIVATE. ~/.dotfiles was clean and master matched remote HEAD e7aea40cd87de3f168a68260888a75766ada8db0. At handoff inspection ~/.pi was clean at 27796a29bfa9de3e2ffb5b879e58b9be311b075b with origin still Algorant/pi. Recheck state before implementation. Task creation does not authorize migration, publication or live changes.