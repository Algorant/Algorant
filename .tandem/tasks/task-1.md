---
id: task-1
type: task
title: "01 — Dotfiles: prepare for public sharing"
state: "validation"
priority: "high"
references: ["https://github.com/Algorant/.dotfiles", "task-11"]
relatedFiles: ["/home/ivan/.dotfiles/README.md", "docs/public-readiness.md", "docs/dotfiles-verification.md"]
tags: ["public-readiness", "dotfiles"]
accord:
  status: "claimed"
  acceptance: ["Record a review of tracked content and Git history for secrets, private data, generated state, and publication blockers without copying sensitive values into findings.", "Replace the README from scratch following Algorant's agreed three-Arch-machine narrative, sysup/tool-ownership explanation, real mise manifest excerpt, bootstrap/profile synchronization description, and linked tool/configuration inventory; do not retain obsolete migration/fallback prose.", "Agree with Algorant on public scope; check documentation, licensing/attribution, setup claims, and live-file/automatic-sync boundaries against actual behavior.", "Address agreed blockers in the authoritative repository and record applicable repository-native checks or explicit validation gaps without modifying this machine's live configuration implicitly.", "Record Algorant's approval of the public-facing result or explicit decision to keep it private/defer; do not publish or change visibility as part of implicit approval."]
  claimedAt: "2026-09-12T04:09:48Z"
  constraints: ["Do not edit live dotfiles, run bootstrap/sync, push, rewrite history, or change GitHub visibility without explicit authorization.", "Follow the checkout's own instructions and existing Tandem workflow for repository implementation; preserve unrelated work.", "Algorant chose one public dotfiles repository with secrets outside Git, not separate maintained public/private dotfiles repositories. task-11 owns the remediation and verification prerequisite; its completion gates public readiness, not the ability to draft the README."]
  updatedAt: "2026-09-12T04:32:40Z"
createdAt: "2026-09-12T03:56:43Z"
updatedAt: "2026-09-12T14:57:46Z"
assignee: "pi"
blockers: ["task-11"]
validation.criterion: "Record Algorant's approval of the public-facing result or explicit decision to keep it private/defer; do not publish or change visibility as part of implicit approval."
validation.note: "Task-11 is complete: README replaced, active history cleaned, fresh-clone checks pass except the reviewed non-credential false positive, and all three main machines are healthy/synchronized. Repository remains private. GitHub's authenticated owner API still resolves an old session-containing commit outside the cleaned refs; no anonymous-access or old-file-content test was performed. Algorant should decide whether to request GitHub Support's retained-object/session-data purge before changing visibility. This is a publication decision, not a secrets-manager implementation task."
validation.requestedAt: "2026-09-12T14:57:46Z"
validation.reviewer: "Algorant"
---
First repository, explicitly prioritized by Algorant. GitHub: https://github.com/Algorant/.dotfiles (private). Authoritative ordinary checkout: /home/ivan/.dotfiles; live configuration is owned separately by mise tracking. Coordinate this outcome here; repository implementation follows dotfiles' own instructions and Tandem workspace.

Algorant's README brief: replace the README entirely, with no obligation to preserve old prose, migration instructions or fallback narratives. Introduce three Arch machine roles generically (desktop/WSL, laptop/Niri+Noctalia, main homelab/headless); explain and link sysup; explain reduced AUR reliance and mise for fast-moving tools; include a representative real manifest; explain mise bootstrap automatic sharing and intentional profile variants; finish with a linked bullet inventory of tools/configurations. Evaluate fnox rather than implicitly adopting it.

Read-only verification completed; evidence is in docs/dotfiles-verification.md. Existing checkout ca8e589 is behind fresh GitHub master 53c1c9c; it was left untouched. Latest remote and laptop tracked snapshots had zero Gitleaks findings, but a full mirror scan of 1,507 reachable commits found historical OpenAI/Anthropic/Exa credential material and an expired OpenAI OAuth JWT in an old agent session. One additional scanner match was a coordination-identifier false positive. No values were recorded or tested against providers. PUBLICATION REMAINS GATED on revocation/rotation confirmation and an agreed history/publication strategy.

Current sysup version matching live laptop/homelab files passed its 49 isolated stub assertions; routine upgrades exclude Rust and four coding agents. fnox 1.35.1 is installed for evaluation; the documented secrets workflow is still SecretSpec/Proton Pass. Laptop and homelab profile counts are 105 and 84 respectively; inspected shared files match. Both systemd watcher services are active, but mise status reports declared-not-running; that discrepancy remains unverified. Desktop SSH name did not resolve, so its live state remains unchecked.

Next direction belongs to Algorant: credential remediation and publication boundary, optional fnox adoption, watcher/desktop verification, then README implementation based on current facts. Do not infer permission for any live changes, history rewrites, pushes or visibility changes.