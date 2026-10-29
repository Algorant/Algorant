# Sharing framework

Algorant's policy (revised 2026-10-29): only genuinely personal things are private. Everything else in a repository may be public.

Roles: this repository owns the policy and the portfolio. gitguard (`Algorant/gitguard`, its own Ceph) owns the tool. Each project's Ceph owns its content. Algorant decides each publication.

## Private

1. **Credentials and secrets:** API keys, tokens, passwords, private keys, session cookies, and similar values that grant access.
2. **Personal records:** family members' names, accounts and details; home address; financial data (statements, transactions, budgets, as in finanza's data or obsmd's former finance inputs); health information; private correspondence.

These never go into a repository that is or may become public, in any branch, tag, board record or commit. Where a project needs such data, it stays outside git (the vault, `~/.config`, fnox and Proton Pass, the homelab database) or the repository stays private.

## Fine to publish

Machine names, the username and home paths, tailnet and MagicDNS names, LAN IP addresses, the homelab domain and service hostnames, and the commit-author email. These need no redaction, mapping or review.

## History

Only a leaked secret justifies rewriting or restarting history, and the secret is rotated as well. Nothing else needs fresh history. If a repository's history holds personal records, it stays private (obsmd).

## gitguard

gitguard blocks credentials and personal records on push, and its Jev step asks only about personal records. A repository is ready to publish when gitguard finds neither in its current tree or history (or a leaked secret has been rotated and removed), its README is honest, and it has a licence ([AGENTS.md](../AGENTS.md)).

## Publishing convention: reference, not product

Everything Algorant shares is a reference: someone points their agent at the repository to borrow ideas, not to clone and run his setup. Every public repository says so, briefly and without a tour voice:

1. **README, first line after the title:** "This is my personal setup, shared as a reference. Point your agent at it and adapt the ideas; don't clone and run it as-is."
2. **AGENTS.md, a short section at the top** titled "Reading this repo as a reference". AGENTS.md is what coding agents read by default in 2026 (Codex, Claude Code without a CLAUDE.md, Cursor, Copilot, Gemini CLI, OpenCode, Pi). llms.txt indexes websites, not repositories. The section says:
   - what the repository is;
   - the ideas worth borrowing and where they live;
   - what is specific to Algorant's machines, accounts and paths, to adapt rather than copy;
   - that scripts such as `bootstrap.sh` are his own, not an installer for others.

   Where the repository has no AGENTS.md, create one with just this section. The rest of an existing AGENTS.md stays as the project's own agent instructions.

## Readability polish: generic current files

Algorant's specifics invite a visiting agent to copy them, so the current files of a public repository use generic stand-ins where that is simple. This is polish, not a privacy gate: no history rewrite, fresh repository or CI provisioning for it, and a miss never blocks publishing.

- His home directory → `~`.
- Machine nicknames → roles: desktop → workstation; x1nano, algotop → laptop; archbox, dellmini, cart-lab → homelab-server; worktop → work-machine; raspi → raspberry-pi. Machine names are publishable, so the map lives here.
- His domain → `example.com`, or a role such as `homelab.example`.
- Accounts and handles used only as examples → placeholders.

Apply it once as a plain find-and-replace on the current tree. Where a repository is published by a generator (the Pi catalog, Algorant/dotfiles), extend that generator's existing replace list instead; the list may live in the generator's private policy file.

## Going public

The project's Ceph prepares the repository; the portfolio Ceph checks it and records "ready, still private"; Herdra asks Algorant; he gives an explicit OK for that specific flip, at that moment; the owner flips it; the portfolio Ceph checks the result logged out.
