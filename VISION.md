---
description: Algorant's public portfolio: his GitHub profile and the public-readiness state of each project he shares.
---

# Vision

## What this project is

Take Algorant's repositories public, one at a time, simplest first, and make each one genuinely ready before it is shared: an organised README in his own `repo-style-rules`, a plain MIT licence, a gitguard pass, content current with the work, and the private→public mechanism verified to work repeatably. Then share it — a thread, a post, a video — and point the next person at something that works for a stranger. The GitHub profile README is the front door that makes that possible.

His words (2026-11-12): *"the algorant tandem board needs a pass/rework based off of the current work we are doing or have been doing there and what the goal/intention is for that project."*

The work is per repo and sequential. This workspace holds the goal, the order, the readiness bar, and one card per repo with its current state and next step. The changes themselves happen in each project, by that project's own agent.

## Ship works in progress

Every project here took a lot of finagling to get working, and every one is still a work in progress with real bugs and rough edges. That should not keep it private. A project is shared once it is safe to show and honestly described, with its limitations stated. Polish continues in public. Known issues get written down, not hidden or used as a reason to wait.

## What "ready" means

Algorant, 2026-11-09: *"organized nice readme, licence (always generic MIT no fuss), gitguard approved/passed, and having the latest updates along with confirming that private -> public actions work appropriately and consistently."*

1. **README reviewed and overhauled** with him, in his `repo-style-rules`: banner as the title, first person, succinct, licence last as `[MIT](LICENSE)`. This is the heart of readiness; every repo so far got a full rewrite.
2. **Licence**: plain MIT, no deliberation, and every README ends with the same last section, exactly as verdigris and tandem do:

   ```
   ## License

   [MIT](LICENSE)
   ```

   Algorant, 2026-11-17: *"I want that standardized across all my repos."*
3. **gitguard passed** on the tree and history at the current tip.
4. **Current**: the published content matches the work, not a stale snapshot.
5. **Mechanism verified**: the visibility flip, or the generator that produces a public mirror, works repeatably.

A clean security scan is one item to check off, not readiness. Algorant, 2026-11-16: *"dotfiles doesn't have readiness in the sense that it matters. so far we have done a complete review and overhaul of the readme for every single repo, and this one would be no different. it doesn't have any security issues, which is completely differnet and just one more thing to check off. but that isn't the encapsulation of 'readiness'. skip dotfiles we will come back to it because its obviously going to take the longest once you take into accoutn a readme rewrite"*

## The order

Simplest first, in his order. Each card on the board carries that repo's state and next step.

1. **pi** — his Pi configuration, published as a generated catalog from the private `.pi` source. Public since 2026-11-10.
2. **tandem** — agentic task management, "Jira for clankers". Public; the public face shipped at 0.17.7.
3. **verdigris** — a public colour scheme repo: a palette, a real theme file and a screenshot per supported app, plus the Omarchy theme. Rescoping with its own agent.
4. **dotfiles** — his Omarchy machine setup, generated from the private `.dotfiles` source by the `.algOS` publisher. Private, and deliberately last: its README rewrite is still owed and will take the longest.
5. **algOS** — a tailored Omarchy/Arch setup, not an operating system. Public since 2026-11-16 as `Algorant/algOS` (fresh history, `00d2c65`), on Algorant's flip word; the showroom was prepared in private `omarchy-setup`. Private operations, installer, VM proof and publisher live in `Algorant/.algOS` (`~/.algOS`), owned by the algOS Ceph. Mixed-case branding is Algorant's explicit exception to the lowercase style rule. The former `algomarchy-bootstrap` is folded in and archived.
6. **herdra** — his front-door orchestrator. Private until he raises it; not a pending decision.

Side projects (xunfurl, RSSify, retrokit, AlgoPDF, mediafetch, finanza, obsmd) sit on one parked card: they are not this board's work unless he says otherwise.

After the six: sharing. Threads, blog posts and videos about each repo, in the same order, once a repo is ready.

## Channels

| Channel | State |
|---|---|
| GitHub profile ([README.md](README.md)) and public repositories | live |
| Blog ([algorant.dev](https://algorant.dev)) | planned |
| YouTube channel | planned |
| Other sites | planned |

Each public project should be easy to point to from any of these channels. A post or video about a project should link to a repository that works for a stranger.

## Principles

- **Private source, public output.** Where a project's working copy mixes private and public material, the private repository stays authoritative and automation publishes a public version. Private changes flow out without a second copy to maintain.
- **Public only on Algorant's word.** Nothing goes from private to public without his explicit OK for that specific flip, given at that moment. Approved plans, licences, readiness evidence or an agreed publication method never count.
- **Nothing private, ever.** Credentials, personal data, financial details, private vault content, and machine-local state never reach a public repository, including this one and its Tandem board.
- **Honest over impressive.** Public descriptions match what the project actually does today.
- **Each project owns its work.** This repository knows the state of each public project and what stands between it and shipping. The changes themselves happen in each project, by that project's own agent — including what a repo contains and how it looks.

How this is carried out day to day: [AGENTS.md](AGENTS.md).
