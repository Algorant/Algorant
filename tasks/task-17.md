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
updatedAt: "2026-10-27T05:19:01Z"
---

## Description

Requested by Algorant via Herdra (2026-10-27). This repository owns the POLICY (the line between shareable and private, and the portfolio); gitguard (~/Projects/gitguard, its own Ceph) owns the TOOL. End goal: every repository can be public after one initial gitguard verification, and Algorant rarely has to think about it again.

Done so far:
- Draft framework: docs/sharing-framework.md (8210c33). It covers content categories and their public-safe bar, where inherently private content lives, what "verified by gitguard" means, the private-to-public flow, and the decisions for Algorant.
- Calibration material sent to the gitguard Ceph: categories and locations only, with leak / accepted-by-design / false-flag judgements, the why-private answers and the audit history.
- Pilot agreed with gitguard (its task-3, local and log-only, nothing committed in pilot repos): herdra, .pi, omarchy-setup, dotfiles, obsmd, Algorant, finanza, tandem, mediafetch, verdigris with its archive. Jev modes set through Herdra: finanza paths-only, obsmd off with a local financial-document path rule, the work machine excluded, the rest full. Framework updated (6f512a2).

Signed off by Algorant (2026-10-27) as his policy:
- Every flip keeps his explicit OK, given as one "yes" on the gitguard report.
- Machine nicknames are findings, replaced through the generic mapping: workstation, laptop, homelab-server, work-machine, raspberry-pi. The mapping is in the [machines] table of the user-level gitguard literals file, never in a repository. Names that are also ordinary words match only in machine context. Fix-forward: the current tree and board must be clean; history alone doesn't block. gitguard confirmed the design in its task-1 (machine findings are notes until the pilot calibrates them).
- Folded into AGENTS.md's shippable bar (ae3bff1). This repository's own docs and active board were cleaned of nicknames (ae3bff1, d6f2da4); archived records are read-only and stay as history.

Standing rule: nothing goes private to public without Algorant's explicit OK for that specific flip. A green verification is evidence, not authorization, unless he decides otherwise.

Pilot in this repository (Herdra, 2026-10-27): in about a day, gitguard installs log-only pre-push and reference-transaction hooks in this repository's clone on the workstation for about one week (gitguard task-5). They never block, log locally only, and use untracked config. If a push or Tandem sync fails mentioning gitguard, tell the gitguard Ceph.

Pilot progress (gitguard, 2026-10-28): the user-level literals file now holds the homelab domain, the tailnet name and an account name (network/identity class, blocking in block mode), so rules catch them offline. gitguard's later publish-gate task will also check that a candidate repository has no history before its fresh root. A per-repository log→block recommendation will follow gitguard's task-4 calibration.

Calibration (gitguard 0.3.1, task-4, 2026-10-28): finding groups across the 12 pilot mirrors went from 1,080 to 241, with no judged leak lost. Of the 241, 27 are leaks newly recovered by the literals.
- Recommended block (new pushes only): herdra, .pi, Pi catalog, omarchy-setup, obsmd (rules only), Algorant, tandem, mediafetch.
- Recommended log: dotfiles (false flags to accept first) and finanza (its data is its purpose).
- Verdigris: out until its own Gitleaks hook and gitguard have an approved coexistence design.
My policy position:
- Adoption is a commit by each owner.
- Each Ceph gets a refusal instruction first: fix the text, or report the finding ID. Never accept without Algorant.
- Initial accepts go to Algorant as one batch.
- Algorant decides after the phase B addendum (about 2026-11-03), as one package through Herdra.
gitguard filed task-7 (`gitguard verify`, the publish gate) following §3.

Next (agreed with gitguard, its task-5): after phase B (about 2026-11-03), gitguard sends one package. It holds the addendum, the per-repo block/log list (verdigris out), the initial accept batch (location, category and why; the Gmail author marked as already approved) and the one-paragraph Ceph instruction. I forward it to Algorant through Herdra as one decision. Verdigris coexistence comes later: gitguard runs after its Gitleaks hook, keeping both exit statuses.
