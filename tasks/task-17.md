---
id: task-17
uid: 3f2ac786-cb81-4a88-a86f-ff5dc2bc3c15
type: task
title: "Sharing framework with gitguard: policy for publishable-by-default repos"
state: todo
priority: "high"
references: ["https://github.com/Algorant/gitguard"]
relatedFiles: ["docs/sharing-framework.md", "AGENTS.md", "docs/public-readiness.md"]
tags: ["public-readiness", "gitguard", "policy"]
accord:
  status: "ready"
  acceptance: ["Algorant has decided the framework's open questions (flip authorization, Jev exposure per repository, machine nicknames), and docs/sharing-framework.md and AGENTS.md reflect them.", "The pilot repository list and per-repository Jev modes are agreed with the gitguard Ceph and recorded.", "Each portfolio Task records its gitguard verification status once the tool can verify."]
  constraints: ["gitguard owns rules, questions, thresholds and hooks; this workspace only sets policy and records verification.", "No values of findings in this public board or docs: categories and locations only."]
  updatedAt: "2026-10-27T03:06:52Z"
createdAt: "2026-10-27T03:06:52Z"
updatedAt: "2026-10-27T03:12:38Z"
---

## Description

Requested by Algorant via Herdra (2026-10-27). This repository owns the POLICY (the line between shareable and private, and the portfolio); gitguard (~/Projects/gitguard, its own Ceph) owns the TOOL. End goal: every repository can be public after one initial gitguard verification, and Algorant rarely has to think about it again.

Done so far:
- Draft framework: docs/sharing-framework.md (8210c33). It covers content categories and their public-safe bar, where inherently private content lives, what "verified by gitguard" means, the private-to-public flow, and the decisions for Algorant.
- Calibration material sent to the gitguard Ceph: categories and locations only, with leak / accepted-by-design / false-flag judgements, the why-private answers and the audit history.
- Pilot agreed with gitguard (its task-3, local and log-only, nothing committed in pilot repos): herdra, .pi, omarchy-setup, dotfiles, obsmd, Algorant, finanza, tandem, mediafetch, verdigris with its archive. Jev modes set through Herdra: finanza paths-only, obsmd off with a local financial-document path rule, the work machine excluded, the rest full. Framework updated (6f512a2).

Standing rule: nothing goes private to public without Algorant's explicit OK for that specific flip. A green verification is evidence, not authorization, unless he decides otherwise.
