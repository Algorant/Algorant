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
updatedAt: "2026-10-29T03:47:18Z"
---
Requested by Algorant via Herdra (2026-10-27). This repository owns the POLICY (the line between shareable and private, and the portfolio); gitguard (~/Projects/gitguard, its own Ceph) owns the TOOL.

Policy revised by Algorant (2026-10-29): only genuinely personal things are private. docs/sharing-framework.md (ea8e4e3, e805977, 899d893) now says:
- Private: credentials and secrets; personal records (family details, home address, financial data, health, private correspondence).
- Fine to publish: machine names, username and home paths, tailnet and MagicDNS names, LAN IPs, the homelab domain and service hostnames, the commit-author email.
- History: rewritten or restarted only for a leaked secret, which is also rotated. Fresh-history plans are dropped (.pi task-491 cancellation requested).
- Publishing convention, "reference, not product": a README first-line note, plus a short "Reading this repo as a reference" section at the top of AGENTS.md (the file agents read by default).
- Readability polish (not a gate): generic stand-ins in current files (home dir → ~, nicknames → roles, his domain → example.com, example accounts → placeholders), done by one-time replace or the generator's replace list.
- AGENTS.md's shippable bar was updated to match.

gitguard is retuning to the narrowed policy (its task-13, release 0.5.0): it blocks credentials and personal records only; drops the network, machine, path and email findings; Jev covers credential, financial, family, home address, health and correspondence. The Nov 3 package is being reworked to match (pilot/retune.md).

Standing rule: nothing goes private to public without Algorant's explicit OK for that specific flip.

Split decided by Herdra (2026-10-29), framework 1101614:
- Personal-setup repos (Pi catalog, Algorant/dotfiles, omarchy-setup, Herdra, future obsmd guide) get the full convention plus polish.
- Products (Tandem, Verdigris and the theme, mediafetch, AlgoPDF, RSSify, x_unfurl, retrokit) get no "don't run it" note: a licence where missing, and an optional ideas section in AGENTS.md.

Owners briefed directly: pi, algomarchy (dotfiles), omarchy-setup, mediafetch, tandem, verdigris. Herdra takes its own repo plus AlgoPDF, RSSify, x_unfurl and retrokit (no Cephs): MIT LICENSE for x_unfurl, retrokit and RSSify, and removal of RSSify's third-party failed-feed dumps.

Next: re-check once the owners report, then bring Herdra the flip list as one yes/no per repo.

All owners done (2026-10-29). Flip list sent to Herdra as one yes/no per repo:
- Recommend YES: pi, dotfiles together with omarchy-setup, x_unfurl, retrokit, AlgoPDF.
- Recommend WAIT: herdra (until the gitguard 0.5.0 personal-records pass) and mediafetch (until Algorant's 0.1.5 trial).
- Stays private: obsmd, finanza and the private sources.
RSSify token leak closed (subscription inactive; untracked in aa2470f).

Flip list ON HOLD (Herdra, 2026-10-29): no flips until Algorant says so. They will fit the polish-then-share sequence in VISION.md.
