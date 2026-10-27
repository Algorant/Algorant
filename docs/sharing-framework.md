# Sharing framework (draft for Algorant)

Status: **draft, awaiting Algorant's decisions** (marked "Decision" below). It describes where the line between shareable and private lies, so that every repository can be public after one initial verification by gitguard, and stays that way without new reviews.

Roles: this repository owns the policy and the portfolio. gitguard (`Algorant/gitguard`, the project's own Ceph) owns the tool: rules, Jev questions, thresholds and hooks. Each project's Ceph owns its own content. Algorant decides publication.

## 1. Content categories

A public repository is everything a stranger can fetch: the default branch, every other branch (including the Tandem board on `tandem`), tags and the full history of all of them. Each category below must meet its bar in all of it, not only in the current tree.

| Category | Examples | Public-safe when |
|---|---|---|
| Code | source, scripts, tests, CI workflows | No credential values. Personal locations come from the environment or placeholders (`$HOME`, `~`, `<user>`), never literals. Vendored third-party code keeps its licence. |
| Config | dotfiles, mise, app and theme configs, `.env.example` | Same as code. Secrets appear only as references (fnox or environment variable names, `.example` placeholders). Host-specific values live in an untracked override or a private companion. |
| Docs | README, AGENTS.md, VISION.md, plans, research notes | No username-bearing paths, no tailnet or MagicDNS names, LAN or CGNAT IPs, or internal domains. Bare machine nicknames (`desktop`, `x1nano`) are acceptable. Links to private repositories are marked as private or removed. |
| Board | Tandem Tasks, Decisions, rules, events, logs | Same as docs. Evidence cites paths, commits and categories, never values, and never local URLs or home paths. A public repository's board is public. |
| Personal data | names other than "Algorant", emails, phone numbers, postal addresses, account or card numbers, family, health or finance prose | Never present. Exception approved by Algorant: his Gmail as commit author. |
| Data files | statements, transaction exports, vault notes, session transcripts, provider payloads, caches, databases | Never in git, in any repository that may become public. See section 2. |
| Media | screenshots, recordings, wallpapers | A person checks each one for visible private details (window titles, notifications, hosts, file names). No tool verdict is enough for images. |
| Commit metadata | author and committer, messages, file names | Same as personal data and docs. File names count: a statement filename is a finding even when its content is binary. |

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
2. **Initial full scan.** A scan of the full history of every ref exits 0 with no unscanned chunks (gitguard's working definition), using the Jev mode set for that repository. Every remaining finding is either fixed or accepted by Algorant with a reason in the accept file.
3. **Fresh history if needed.** If history holds a leak, the repository is republished from a clean tree as a new single-commit history, with the old history kept private in `<name>-archive`. Existing published history is not rewritten in place. The fresh repository is then scanned again (step 2).
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

## 5. Decisions for Algorant

1. **Is a green verification enough to flip?** Today's rule: nothing goes private to public without his explicit OK for that flip, at that moment. Proposal: keep that one confirmation, but reduce it to a single yes on a gitguard report, since everything before and after it is automated. Optionally, later, after the pilot has run without misses: pre-authorize repositories that pass verification with no accepted personal-data findings. That is his call.
2. **Jev data exposure per repository**, from Herdra research task-42: `full` for ordinary repositories, `paths-only` or `off` where the content is itself sensitive (finanza, obsmd, worktop machines).
3. **Bare machine nicknames** in public docs and boards: accepted by design (proposed), or treated as findings.

## 6. Pilot

Coordinated with gitguard (its task-3, log-only). It is chosen to cover each category and each judgement: known leaks (Tandem board, Herdra research, mediafetch test, obsmd file names), accepted-by-design values (machine nicknames, the approved author email), false flags (vendored bundles, placeholder tokens) and clean controls (omarchy-setup, the fresh Verdigris).
