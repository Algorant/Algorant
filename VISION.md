---
description: Algorant's public portfolio: his GitHub profile and the public-readiness state of each project he shares.
---

# Vision

This repository holds what it takes to keep Algorant's public-facing projects current and presentable, and to connect them to the places he shows up online. The GitHub profile README is the most visible part of it, but only one part. When Algorant works on his public presence, the full picture should be here.

## Ship works in progress

Every project here took a lot of finagling to get working, and every one is still a work in progress with real bugs and rough edges. That should not keep it private. A project is shared once it is safe to show and honestly described, with its limitations stated. Polish continues in public. Known issues get written down, not hidden or used as a reason to wait.

## Channels

| Channel | State |
|---|---|
| GitHub profile ([README.md](README.md)) and public repositories | live |
| Blog ([algorant.dev](https://algorant.dev)) | planned |
| YouTube channel | planned |
| Other sites | planned |

Each public project should be easy to point to from any of these channels. A post or video about a project should link to a repository that works for a stranger.

## Projects

First focus, in order:

1. **Verdigris**: an oxidized-copper color theme with ports for the tools Algorant uses. It is the closest to shareable, and a theme is the easiest thing for a stranger to try.
2. **Tandem**: agentic task management ("Jira for clankers"). It is the centerpiece of Algorant's agent workflow, and it already has releases, a site, a logo, and a teaser.
3. **Pi setup**: Algorant's Pi agent configuration, extensions, and skills, published as a generated catalog from a private source. It shows how he actually works with agents, including Pi's codemode.
4. **Dotfiles**: his machine setup, now Omarchy-based and bootstrapped with mise. Algorant decided the generated `Algorant/dotfiles` repository stays private; it is not a publication target.

Next:

5. **Algomarchy**: a public guide or checklist, section by section, to how Algorant customized each important part of Omarchy to fit him.
6. **obsmd**: Obsidian vault maintenance with agents. The repository stays private. If anything goes public, it is a separate, generic guide to setting things up the same way (skills, scripts), written fresh with no secrets or personal content. Not scheduled.

Later:

7. **mediafetch**: an Obsidian plugin that creates media notes from provider metadata.
8. **finanza rulebook**: how Algorant got his personal finance automation working, written as a reusable rulebook without any personal or financial details.

Also tracked, without changing the focus order above:

9. **[Herdra](https://github.com/Algorant/herdra)**: Algorant's front-door orchestrator agent, a Pi session coordinating project agents over Herdr, Tandem and an agent inbox. It brings back results, decisions and blockers and keeps one focused Now item at a time. The repository is private for now; the link is an intentional placeholder. Public-readiness blockers are unknown until reviewed.

Older profile projects (xunfurl, RSSify, retrokit, AlgoPDF) stay listed but are not a current focus.

## Principles

- **Private source, public output.** Where a project's working copy mixes private and public material, the private repository stays authoritative and automation publishes a public version. Private changes flow out without a second copy to maintain.
- **Public only on Algorant's word.** Nothing goes from private to public without his explicit OK for that specific flip, given at that moment. Approved plans, licences, readiness evidence or an agreed publication method never count.
- **Nothing private, ever.** Credentials, personal data, financial details, private vault content, and machine-local state never reach a public repository, including this one and its Tandem board.
- **Honest over impressive.** Public descriptions match what the project actually does today.
- **Each project owns its work.** This repository knows the state of each public project and what stands between it and shipping. The changes themselves happen in each project, by that project's own agent.

How this is carried out day to day: [AGENTS.md](AGENTS.md).
