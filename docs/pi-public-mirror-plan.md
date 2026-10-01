# Pi public mirror plan

## Decision and ownership

Algorant chose a private source plus generated public showcase; no further architecture assessment is needed.

- Rename the existing private `Algorant/pi` repository to `Algorant/.pi`, preserving its history and coordination state.
- Keep `~/.pi` as the authoritative local checkout and live setup; do not relocate it.
- Create a new repository at the freed `Algorant/pi` identity for sanitized output with independent clean history. Do not make the existing private history public.
- Keep publication rules, replacements, and automation in the private source. The public repository is generated output, not a second maintained setup.
- Implementation belongs in `~/.pi`'s Tandem workspace, where `task-182` (Prepare private .pi source and generated public Pi showcase) owns the outcome and requires a scoped plan before implementation. This repository's `task-2` tracks independent portfolio verification. Bounded implementation Tasks or milestones will follow the Pi workspace's planning checkpoint.

## Verified baseline

At planning time, read-only Git and GitHub checks confirmed:

- `~/.pi`: origin `Algorant/pi`, PRIVATE, local `main` and remote HEAD both `5c8826976f758c3c3b618327d0334ee4078c2e56`. Existing uncommitted Tandem records must be preserved.
- `~/.dotfiles`: origin `Algorant/.dotfiles`, PRIVATE, clean checkout, local `master` and remote HEAD both `e7aea40cd87de3f168a68260888a75766ada8db0`.

The dotfiles reference is `scripts/public-dotfiles/`, `public/`, `.github/workflows/publish-dotfiles.yml`, and `scripts/tests/test-public-dotfiles.sh`. Recheck repository state before execution; this is a snapshot, not a lock.

## Implementation sequence

### 1. Define public scope and migration touchpoints

Read Pi's own instructions, Tandem rules, and relevant active work before creating implementation Tasks. Use bounded read-only Subagents for public-resource selection and repository-reference mapping.

Select reusable extensions, skills, themes, configuration examples, and documentation explicitly. Exclude conversations, sessions, memories, coordination records, credentials, caches, logs, installed packages, and other private/runtime state by path; do not inspect their contents or audit their private history.

Review only selected public material for embedded credentials, personal identifiers, local paths, private repositories, hosts/endpoints, and unavailable dependencies. Identify affected Git remotes, package/install references, automation, and documentation. Distinguish private source references from links that should continue pointing at the public showcase.

### 2. Implement and test the private publisher

Adapt the relevant dotfiles mechanisms to the approved Pi scope: export allowlisted committed resources into a temporary tree, apply omissions and deterministic replacements, add public metadata, audit the output, and update the destination only after checks pass. Keep private rules out of generated output and avoid modifying live configuration to sanitize it.

Use direct inspection and narrowly scoped temporary synthetic checks for concrete risks: exclusions, replacements, additions/deletions, repeatable no-op output, rejected output leaving the destination unchanged, safe diagnostics, and applicable path/binary/symlink handling. Pi's current rules prohibit default broad-suite runs and new permanent tests or reusable harnesses without explicit approval. Follow those rules; dotfiles test results are reference material, not Pi evidence.

### 3. Prepare the public presentation

Write the public README and reusable configuration examples against the tested output. Explain what is reusable, prerequisites, installation/reference usage, limitations, licensing/attribution, and the generated nature of the repository. Do not imply that cloning the showcase reproduces private services or the entire live setup.

### 4. Execute the approved repository switchover

Present the exact cutover steps to Algorant before executing remote or live changes. Verify destination-name availability and identify affected consumers first.

Rename the existing private repository to `Algorant/.pi`, update the authoritative checkout's remote and required references, then create the replacement `Algorant/pi` as private initially. Initialize it from the validated snapshot with clean independent history and public-safe commit identity. Do not rely on GitHub's old-name redirect once `Algorant/pi` is reused. Verify private history and local state remain intact; do not delete or rewrite the source history.

### 5. Connect and verify publication

Add the private-source GitHub Action with narrowly scoped access to the public destination. Verify successful publication, blocked unsafe output, deletion propagation, and no-op behavior without logging private values.

Inspect a fresh clone of the generated repository and its history before requesting approval to make it public. After approval, verify anonymous access and the documented public experience. Reload affected Pi sessions if live resources or context changed.

### 6. Close the portfolio loop

Accept implementation work in Pi's own workspace first. Independently verify the private/public identities, publication outcome, and public README here. Update `docs/public-readiness.md`, link implementation Task IDs and concise evidence from `task-2`, and complete that portfolio Task only after Algorant approves the outcome. The profile's existing `Algorant/pi` link should remain the public-facing URL.

## Boundaries

This plan authorizes planning only, not repository renames/deletions, pushes, visibility changes, history rewrites, or live configuration edits. Public-output validation replaces a broad examination of excluded private data; it does not certify erasure of previously hosted data. Prefer the rename-and-new-output path rather than copying dotfiles' destructive recreation helper.
