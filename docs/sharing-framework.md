# Sharing framework

Status: **signed off by Algorant as his policy (2026-10-27)**, with machine nicknames treated as findings (below). It describes where the line between shareable and private lies, so that every repository can be public after one initial verification by gitguard, and stays that way without new reviews.

Roles: this repository owns the policy and the portfolio. gitguard (`Algorant/gitguard`, the project's own Ceph) owns the tool: rules, Jev questions, thresholds and hooks. Each project's Ceph owns its own content. Algorant decides publication.

## 1. Content categories

A public repository is everything a stranger can fetch: the default branch, every other branch (including the Tandem board on `tandem`), tags and the full history of all of them. Each category below must meet its bar in all of it, not only in the current tree.

| Category | Examples | Public-safe when |
|---|---|---|
| Code | source, scripts, tests, CI workflows | No credential values. Personal locations come from the environment or placeholders (`$HOME`, `~`, `<user>`), never literals. Vendored third-party code keeps its licence. |
| Config | dotfiles, mise, app and theme configs, `.env.example` | Same as code. Secrets appear only as references (fnox or environment variable names, `.example` placeholders). Host-specific values live in an untracked override or a private companion. |
| Docs | README, AGENTS.md, VISION.md, plans, research notes | No username-bearing paths, no tailnet or MagicDNS names, LAN or CGNAT IPs, or internal domains. No machine nicknames: use the generic names from the machine mapping (below). Links to private repositories are marked as private or removed. |
| Board | Tandem Tasks, Decisions, rules, events, logs | Same as docs, including the machine mapping. Evidence cites paths, commits and categories, never values, and never local URLs or home paths. A public repository's board is public. |
| Personal data | names other than "Algorant", emails, phone numbers, postal addresses, account or card numbers, family, health or finance prose | Never present. Exception approved by Algorant: his Gmail as commit author. |
| Data files | statements, transaction exports, vault notes, session transcripts, provider payloads, caches, databases | Never in git, in any repository that may become public. See section 2. |
| Media | screenshots, recordings, wallpapers | A person checks each one for visible private details (window titles, notifications, hosts, file names). No tool verdict is enough for images. |
| Commit metadata | author and committer, messages, file names | Same as personal data and docs. File names count: a statement filename is a finding even when its content is binary. |

**Machine nicknames.** Algorant's machine nicknames are harmless but do not appear in public material. A mapping list outside every repository, next to gitguard's personal literals, gives each nickname a generic replacement: `workstation`, `laptop`, `homelab-server`, `work-machine`, `raspberry-pi`. It lives in the `[machines]` table of `~/.config/gitguard/literals.toml` (never in a repository, since it lists the nicknames). gitguard flags a nickname and suggests the replacement. Names that are also ordinary words are matched only in machine context (in backticks, host or SSH fields, `name.` or `name:` hostnames, "on/from/to name"). Until the pilot calibrates it, a nickname is reported as a note, not a block (gitguard task-1).

*Exception (approved by Herdra, 2026-10-29, `.pi` task-490):* the private `.pi` repository's publisher policy (`public/pi-public.json`) may hold nickname-to-generic redaction rules derived from the machine mapping. Reason: CI regenerates the public Pi catalog on GitHub, and reading the user-level mapping there would need new secret provisioning. The exception is narrow: the rules stay in that private source, are used only to redact generated output, and are never exported. The mapping itself still lives only in the user-level file. Any other repository needing the same must get its own approved exception. A nickname is a fix-forward finding: the current tree and board must be clean, but a nickname only in history does not force fresh history.

Findings are judged in three ways (calibration vocabulary shared with gitguard):

- **leak**: must not be public. Fix it before publishing, and if it is already in history, use fresh history (section 3).
- **accepted by design**: a value that is safe to publish, recorded once in gitguard's accept file with a reason. Only Algorant accepts.
- **false flag**: the pattern matched something that is not private (vendored bundles, placeholders, third-party data). The tool should learn to skip it.

## 2. Where inherently private content lives

The repository itself must be publishable, so content that is private by nature never enters it:

1. **Out of git (default).** Personal data stays where it already lives: the Obsidian vault, `~/.config`, the homelab database, fnox and Proton Pass. Repositories read it through configuration at run time. Working directories for such data are git-ignored, and gitguard's path rules catch them if the ignore is missing.
2. **Private companion repository**, when private material needs version control: a separate private repository such as `.pi` (source of the generated `Algorant/pi`), `.dotfiles` (source of the generated dotfiles), `Algomarchy` (operations), or `<name>-archive` (old history, as Verdigris did). Public repositories do not depend on a companion to work, and do not link to it as if visitors could follow.
3. **Repositories whose content is the private thing** (finanza's data, obsmd's vault material) stay private as a whole. What goes public is new, generic material written for strangers: the finanza rulebook, the future obsmd setup guide.

## 3. "Verified by gitguard"

A repository is verified when all of these hold, recorded on its portfolio Task:

1. The repository has committed gitguard's config.
2. **Initial full scan.** A scan of the full history of every ref exits 0 with no unscanned chunks (gitguard's working definition), using the Jev mode set for that repository. Every remaining finding is either fixed or accepted by Algorant with a reason in the accept file. Machine nicknames in the current tree and board are replaced with their mapped generic names; nicknames only in history do not block.
3. **Fresh history if needed.** If history holds a leak, the clean tree is published as a **new repository** with a single-commit history, and the old repository is renamed to `<name>-archive` and stays private. History is never rewritten or force-pushed in place: GitHub keeps serving unreachable commits by SHA until a support purge or the repository is deleted, so a rewritten repository that later turns public would still expose them (gitguard pilot, 2026-10-28). The new repository is then scanned again (step 2). Verdigris followed this route on 2026-10-26: `Algorant/verdigris` is a new repository, and its old commits return 404 anonymously.
4. **Hooks on.** The pre-push and reference-transaction hooks are installed on every clone that pushes (or by the machine-wide dispatcher once that exists). The scheduled all-refs scan is enabled for the repository.
5. **Record.** The portfolio Task records the gitguard and ruleset versions, the date, the scanned refs and the result. A ruleset major version change means a new full scan.

Verification covers text and file names. It does not replace the person's check of media (section 1) or the README's honesty about limitations (AGENTS.md shippable bar).

## 4. Moving a repository from private to public

1. The project's Ceph prepares it: licence (MIT, copyright Algorant, unless the project inherits another), a work-in-progress README with known issues and working instructions, and no links that only work for Algorant.
2. gitguard verification is green (section 3).
3. The portfolio Ceph checks the shippable bar and the media, and records "ready, still private".
4. Herdra asks Algorant for the explicit OK for that specific flip, with the gitguard report attached.
5. After his OK, the owner flips visibility. The portfolio Ceph checks the result logged out (anonymous page, clone, links), updates the profile and the Task.

Already-public repositories need no new review: the hooks and the scheduled scan keep them clean, and a finding is handled as a normal fix.

## 5. Decisions (Algorant, 2026-10-27)

1. **Flip gate:** every private-to-public flip keeps his explicit OK, given as one "yes" on the gitguard report for that flip. Revisited after the pilot only if he raises it.
2. **Jev data exposure per repository.** Already set through Herdra (2026-10-27): `full` for ordinary repositories, finanza `paths-only`, obsmd `off` (rules only, with a local rule for financial-document paths), the work machine excluded. Values are always masked before sending. Algorant can change any repository with one config value.
3. **Machine nicknames:** not accepted by design. They are replaced through the machine mapping (section 1).

## 6. Pilot

Agreed with gitguard (its task-3): herdra, .pi, omarchy-setup, dotfiles, obsmd, Algorant and finanza (Algorant's list), plus tandem, mediafetch and verdigris with its archive. The pilot is local and log-only: per-clone untracked config, hooks in each clone's git dir, nothing committed or pushed in pilot repositories.

It covers each category and each judgement: known leaks (Tandem board, Herdra research, mediafetch test, obsmd financial file names, which the new local rule must catch offline), accepted-by-design values (machine nicknames, the approved author email), false flags (vendored bundles, lockfile emails, placeholder tokens, third-party feed contacts) and clean controls (omarchy-setup, the fresh Verdigris).
