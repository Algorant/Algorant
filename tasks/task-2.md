---
id: task-2
uid: dae194be-bd7a-4d67-9192-1b94ddd630c6
type: task
title: "03 — Pi setup: publish the generated catalog"
state: todo
references: ["https://github.com/Algorant/pi"]
relatedFiles: ["docs/pi-public-mirror-plan.md", "docs/public-readiness.md", "README.md", "/home/ivan/.pi/README.md", "/home/ivan/.pi/.tandem/tasks/task-182.md"]
tags: ["public-readiness", "pi"]
accord:
  status: "ready"
  acceptance: ["Record the approved public-resource scope and migration touchpoints; exclude private/runtime paths without inspecting their contents or auditing private history, and review selected public material plus generated output/history without exposing sensitive values.", "Implement and verify the approved private Algorant/.pi source and generated Algorant/pi architecture in the authoritative ~/.pi workspace, preserving private history and unrelated local work; obtain explicit approval before remote cutover, publication, or live changes.", "Verify public documentation, licensing/attribution, reusable configuration and usage claims against generated output; record Pi-native publication checks and explicit validation gaps.", "After implementation is accepted in Pi's own workspace, independently verify local and remote outcomes, update the portfolio documentation, and record Algorant's approval before completing this coordination Task."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials, personal or financial details, vault content, or home-directory paths."]
  updatedAt: "2026-10-12T01:50:20Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-10-12T01:50:20Z"
priority: "high"
---
## State

The private source is Algorant/.pi (checkout ~/.pi). The 'Publish Pi snapshot' Action regenerates Algorant/pi on every main push (green on 2026-10-11). But Algorant/pi is still PRIVATE, so the profile's 'My Pi Setup' link 404s. Recent features: agent inbox, Herdra widget, model roles with quota-aware choice, an adversarial reviewer, dbs, /mem. Codemode is used throughout. Algorant expects a significant codemode-driven refactor, which does not block publishing.

## Shippable means

The common bar in AGENTS.md, plus: the public README explains the codemode-based tool model wherever it matters, and states the pending refactor as a known limitation.

## Crippling issues

1. The generated Algorant/pi is private, so the link is dead.
2. The public README and output have not been reviewed since codemode, model roles, and the inbox landed. The codemode-awareness of the public text is unknown.
3. Open Worker and Subagent reliability bugs on the .pi board (task-405, task-409, task-410) affect anyone copying the delegation setup.
(Inferred read-only; not yet confirmed with the .pi Ceph.)

## Next step

The .pi Ceph reviews a fresh clone of the generated Algorant/pi (safety, README, codemode accuracy) and reports. Then Algorant decides on making it public.
