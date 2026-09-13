# GitHub public-readiness review

## Scope and intent

Algorant authorized this repository to be the Tandem coordination hub for preparing the projects linked in [`README.md`](../README.md) for public sharing. The target is safe, useful, honestly described public work—not an assumption that every project must become production-ready or public.

Review one repository at a time with Algorant. Each row below has its own coordination Task in this workspace. Dotfiles is complete: the private `Algorant/.dotfiles` repository owns a privacy-gated publisher, and the profile now links to the generated public `Algorant/dotfiles` repository with independent clean history. Pi setup is next; the remaining reviews have not started.

## Repository map and review order

GitHub identities and visibility were checked with authenticated `gh repo view`; local identities were checked against each checkout's `origin`. Visibility is an inventory snapshot, not a readiness verdict. Paths beginning with `~` refer to the current user's home directory.

| Order / Task | Profile project | GitHub repository | Authoritative local checkout | Visibility at inventory | Checkout action |
| --- | --- | --- | --- | --- | --- |
| 1 / `task-1` | My Dotfiles | [Algorant/dotfiles](https://github.com/Algorant/dotfiles) | Source: `~/.dotfiles`; generated checkout: `~/Projects/dotfiles` | Public | Generated |
| 2 / `task-2` | My Pi Setup | [Algorant/pi](https://github.com/Algorant/pi) | `~/.pi` | Private | Reused |
| 3 / `task-3` | Tandem | [Algorant/tandem](https://github.com/Algorant/tandem) | `~/Projects/tandem` | Public | Reused |
| 4 / `task-4` | Verdigris | [Algorant/verdigris](https://github.com/Algorant/verdigris) | `~/Projects/verdigris` | Private | Reused |
| 5 / `task-5` | AlgoNix | [Algorant/AlgoNix](https://github.com/Algorant/AlgoNix) | `~/Projects/AlgoNix` | Private | Reused |
| 6 / `task-6` | xunfurl | [Algorant/x_unfurl](https://github.com/Algorant/x_unfurl) | `~/Projects/x_unfurl` | Private | Cloned |
| 7 / `task-7` | RSSify | [Algorant/rssify](https://github.com/Algorant/rssify) | `~/Projects/rssify` | Public | Cloned |
| 8 / `task-8` | retrokit | [Algorant/retrokit](https://github.com/Algorant/retrokit) | `~/Projects/retrokit` | Private | Cloned |
| 9 / `task-9` | mediafetch | [Algorant/mediafetch](https://github.com/Algorant/mediafetch) | `~/Projects/mediafetch` | Private | Cloned |
| 10 / `task-10` | AlgoPDF | [Algorant/AlgoPDF](https://github.com/Algorant/AlgoPDF) | `~/Projects/AlgoPDF` | Private | Reused |

All ten checkouts are present. The four new clones include normal Git history (not shallow clones), have the expected origin, and were clean after cloning. Existing checkouts were not pulled, reset, relocated, or modified during inventory; an origin match does not establish that an existing checkout is current with GitHub.

The profile describes two groups:

- **Dev Setup/Tools:** shared Pi configuration; mise-powered dotfiles; agentic task management; a preferred colorscheme; and essential Linux tools.
- **Some Projects:** Twitter/X previews for Slack; podcast RSS updates to Slack; ROM collection/device synchronization; Obsidian media notes; and a Linux-first offline PDF reader derived from NightPDF.

Other local projects, including `herdr`, `ketch`, `obsmd`, and `verdigris.nvim`, are not currently linked in the profile README and were not added to this review queue. Add or remove scope deliberately with Algorant.

## Review rubric

For each repository:

1. **Establish scope and ownership.** Read its instructions, README, existing Tandem rules and relevant manifests. Agree with Algorant on the intended audience, supported use, and what should remain private.
2. **Review publication safety.** Inspect tracked files and Git history for secrets, private data, machine-specific information, generated/runtime state, and problematic assets. Record locations and remediation without reproducing sensitive values. A clean working tree is not proof of a safe history; rewriting history or rotating credentials requires explicit direction.
3. **Check presentation and rights.** Verify the README's promises against implementation; clarify experimental status, limitations, installation, configuration, examples, licensing, attribution, and asset/dependency rights.
4. **Agree on and implement bounded fixes.** Record concrete blockers and follow-up work after inspection. Use the authoritative repository, preserve unrelated edits, and keep implementation under that repository's own workflow. A coordination Task here is not a cross-repository Worker assignment.
5. **Validate honestly.** Use only that repository's applicable test/build/check commands, following its own rules. Record what was exercised, actual outcomes, and any missing credentials, hardware, fixtures, or manual checks. Do not run setup, deployment, sync, or live configuration changes implicitly.
6. **Obtain Algorant's decision.** Record approval of the public-facing result, or a decision to defer/keep private. Readiness approval is distinct from permission to push, rewrite history, or change GitHub visibility.

## Initial cautions

- **Dotfiles:** implementation and publication controls live in the private `~/.dotfiles` source workspace. Its GitHub Action generates the public repository from canonical snapshot roots, applies private omissions/replacements, audits the staged tree, and publishes only approved output. The public repository is not a second source of truth.
- **Pi setup:** `~/.pi` is the canonical shared configuration repository. Do not create a competing clone under `Projects`; keep credentials, installed packages, sessions, caches, logs, and other runtime state out of public material. Review before changing live resources.
- **AlgoPDF:** pre-existing changes were observed in `tsconfig.json` plus untracked `.tandem` event/log files. Preserve them and resolve ownership before implementation. Review NightPDF attribution and derivative licensing.
- **Existing coordination:** dotfiles, Pi, Tandem, mediafetch, and AlgoPDF already have `.tandem` directories. Read their rules and active work when each review begins. No additional repository workspaces were initialized during inventory.
- **Profile draft:** the existing `README.md` was untracked at inventory and was left unchanged. No repositories were pushed or had their visibility changed.

## Adding a project later

Confirm its intended GitHub identity and place in the review order with Algorant. Match by Git remote, not directory name. Reuse an authoritative existing checkout; otherwise clone into `~/Projects` without overwriting an existing path. Add a coordination Task with acceptance criteria and update this map. Do not treat inclusion as permission to publish.
