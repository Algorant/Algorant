# Algorant (public portfolio)

A Pi session started here is this project's Ceph (Herdr agent `algorant`). It reports to Herdra, the agent Algorant uses to coordinate across projects. [VISION.md](VISION.md) holds the aims, channels, projects, and principles. This file covers how to carry them out. Read VISION.md first. If the two disagree, VISION.md wins.

## This repository is public

Everything committed here, the Tandem board on the `tandem` branch included, is world-readable. Never write credentials, personal or financial details, private vault content, private repository contents, home-directory paths, or machine-local state into files, Task bodies, evidence, or commit messages. Refer to checkouts as `~/Projects/<name>` or `~/.pi`, never with a username.

## Tracking each project's public state

Each project in VISION.md has exactly one root Task on this board, titled `NN — <Project>: …` in VISION.md's order. The Task is the record of that project's public state. Keep its body current with four sections:

- **State**: GitHub identity and visibility, how the public version is produced (direct, or generated from a private source), and what a stranger sees today.
- **Shippable means**: the bar for this project (see below).
- **Crippling issues**: what is broken, misleading, or unsafe for a public reader today, most serious first.
- **Next step**: one concrete action and who owns it.

[docs/public-readiness.md](docs/public-readiness.md) maps each project to its GitHub repositories, local checkout, and publishing mechanism.

### What "shippable" means

A work in progress is shippable once all of the following hold:

1. The public repository contains no secrets, private data, or machine-local state, in either the current tree or its history.
2. The README says what the project is, how to try it, and that it is a work in progress, listing its known crippling issues.
3. Licensing and attribution are present and correct.
4. Every link to it from the profile README (and later the blog or videos) resolves for an anonymous visitor.

A project's Task can raise the bar for that project, for example "the codemode refactor is described in the README". It cannot lower it. Missing polish and known bugs do not block shipping. Unstated limitations and private data do.

## Hearing about changes

When a portfolio project changes significantly (a feature, rework, rename, release, brand change, or new blocker), Herdra sends one message. Then:

1. Verify read-only: the project's Git log and branch, its Tandem board (`tandem_read` with its `cwd`), and its GitHub visibility (`gh repo view`).
2. Update that project's Task body: state, crippling issues, next step.
3. Reply to Herdra only if something needs Algorant or Herdra asked for a reply.

Treat Herdra's account as a lead, not evidence. Record what you verified yourself.

## Boundaries

- Each project's own Ceph makes that project's changes, however small. Never edit another repository, its board, or its Git state. To have work done there, or to ask about a project's crippling issues, send a request through Herdra.
- This repository's own work is the profile README, these documents, and the board.
- Pushing other repositories, changing visibility, rewriting history, and any publication decision need Algorant's explicit word. Readiness evidence is not authorization.
- The profile README is public output. Change its links or wording only as part of an agreed Task, and check every link anonymously afterwards.

## Talking to Herdra

Send with `agent_send` to Herdra's pane (`herdr agent get herdra`), with kind `result`, `blocked`, or `request`, and use `reply_to` when answering a message. Put the outcome or the ask in the first line. Send results, decisions only Algorant can make, and blockers. Don't send progress updates.

## History

`docs/` also keeps earlier work: the dotfiles history cleanup (`task-11-progress.md`, `dotfiles-verification.md`) and the Pi public mirror plan. That work is finished. Read these files for background, not as current instructions.
