# Task 11 — remediation investigation progress

Task: `task-11` in the Algorant portfolio workspace. Owner: Pi, working directly at Algorant's request. **This is interim evidence, not a completed remediation or permission to publish.**

## Current status — cleanup applied and verified

Algorant approved the coordinated production cutover. It completed successfully: verified private Git bundles were created on all three machines, all writers were stopped, only `master` and `niri-config` were replaced in one atomic push with exact old-SHA leases, all three ordinary checkouts and native mise history stores were refreshed, and every restore verified before publishers resumed. `ArchWSL` remained unchanged. The repository is **still private**.

The new README is on GitHub and all three checkouts. Both TOML examples match actual configuration, all 31 local links resolve, and its secret scan passes. Local task-29/task-30 records and the entire current Tandem tree were preserved without modifying archived record content.

Final independently scanned remote HEAD: `fc77896bc0a3ed72a4ead1baa46373e6995d3712`. All three live history stores and their upstream refs converged to that same clean HEAD. Each machine has one running mise 2026.9.5 watcher, no pending sync errors, and the expected 105/84/84 active paths. Global mise configuration and shared Zsh content were preserved byte-for-byte; the obsolete secret file/loader remain absent. The active ordinary checkouts are clean.

The fresh remote clone has zero current-tree Gitleaks findings. Its history has only the previously reviewed non-credential handoff identifier; the original affected commit objects are absent from the clone and `git fsck --full` passes. The candidate had also been checked across all 6,981 Git objects for exact revoked values, finding none.

**Hosting limitation:** an authenticated owner API check can still resolve the old session-containing commit `6fea5b0bdcba...` on GitHub, despite its absence from the fresh clone and all active refs. No old file contents or anonymous/public access were tested. History rewriting does not certify removal of GitHub's retained/cached objects. Algorant confirmed the old API keys revoked; any desired server-side purge of old session data belongs to GitHub Support. Keep this distinction explicit in the separate publication decision.

Private recovery material on each machine: `~/.local/state/dotfiles-cleanup-20260912-approved-cleanup/` contains verified bundles/receipts; `~/.dotfiles-before-20260912-approved-cleanup` preserves the retired complete checkout, including ignored local files and stashes; `~/.local/state/mise/history-before-20260912-approved-cleanup` preserves the retired history store. The retired ordinary clone's push URL is disabled. Desktop's 10 and homelab's 7 recorded stash entries were preserved, not reapplied into public history. Do not reactivate old history stores or push these recovery copies.

Operation and final evidence: `/tmp/dotfiles-cutover.KkYk5q/receipt.json`, `final-scan/safe-summary.json`, and `github-retention.json`; final per-machine verification is `/tmp/dotfiles-safety-fixes.KwOfTX/verification.json`. The approved cutover script and final verification both exited 0. A pre-cutover isolated test caught existing tracking configuration seeding unrelated history; the tested procedure temporarily set that configuration aside and restored it byte-for-byte through native adoption. No production failed adoption was attempted.

Algorant excluded deprecated x1nano and narrowed this work: fnox migration and additional security-infrastructure work were not performed or made blockers. No successful Subagent or Worker delivery was involved. The sections below retain earlier evidence and proposals; this current-status section supersedes their old pending-state descriptions.

## Decisions and completed live safety fixes

Algorant confirmed that the historical OpenAI, Anthropic and Exa API keys are revoked and may be removed from history. Algorant selected **native GitHub push protection with its documented coverage limits**, not mandatory local Gitleaks on every mise push. That changes the prevention scope; the GitHub control still needs configuration/verification before publication.

After the exact desktop file was identified, a read-only check established that `~/.config/zsh/.secrets` contained only the same revoked OpenAI key, no other statements, and that its sole reference in the inspected Zsh configuration was the shared loading line. Algorant explicitly approved deleting that file and removing the shared loader, including normal mise synchronization. The earlier permissions-only proposal was superseded, not implemented.

Algorant also explicitly approved upgrading mise to the tested 2026.9.5 release and restarting its watcher on all three machines. This limited implementation was recorded and completed as **task-29 in the dotfiles workspace**, independently of this still-open portfolio Task.

Completed and independently verified:

- All three old watcher processes were stopped and their absence confirmed before any binary update.
- Native `mise self-update 2026.9.5 --yes --no-plugins` updated each standalone installation; each binary matched the official tested asset's SHA-256.
- The obsolete loading block was removed from the authoritative live laptop `.zshrc`; the revoked desktop-only `.secrets` file was deleted without creating another plaintext copy.
- The approved Zsh change reached desktop and homelab through native mise synchronization and `pull --yes`, not edits to checkout snapshots.
- All three now report mise **2026.9.5**, **one running watcher**, an intact state-directory `history/watch.lock`, no deleted held locks, and no sync errors/pending operations. Active tracking counts remain **105/84/84** for laptop/desktop/homelab.
- `.secrets` is absent on all three inspected machines, the loader is absent from all three live Zsh files, and `zsh -f -n` passes on each. Shared SHA-256: `dcbc8a700325a35e99ee60bed90238b3576ad5790a338fc816218a6d0633afba`.
- Fresh remote `master` at `9d92f350dea842df8c0fbc80fcb108f234cdadce` differs from the pre-change tree only in `home/.config/zsh/.zshrc`, matching the live hash. Local history checkpoint IDs can differ after native pull; this is not a claim that every local ref is identical.
- Repository-native `bash scripts/sysup/tests/test-sysup-rust-optin.sh` exits 0 with **49 passed, 0 failed**; external commands are stubbed. No full `sysup` or unrelated upgrades ran.

Operational evidence: `/tmp/dotfiles-safety-fixes.KwOfTX/results.json` and `verification.json`. The coordinated script's first desktop restart check raced startup; inspection confirmed the service had started, and restart verification resumed without restarting it twice. An initial noninteractive pull omitted `--yes`, returned 0 without applying the pending change, and was caught by the content assertion; the approved command was corrected and final verification passed. No machine was left stopped or partially upgraded.

Recoverable non-secret backups of the former mise executable and Zsh configuration are in each machine's owner-only `~/.local/state/dotfiles-safety-fixes-20260912/`. Existing shells may retain the revoked environment variable until restarted or unset. No existing Git history was rewritten, and no GitHub visibility or security setting was changed by this phase; normal mise commits recorded the approved Zsh change.

## Baseline investigation (before the approved live fixes)

### All three machines are accessible and inventoried

The previous desktop access gap is resolved without changing SSH configuration or host trust. The existing known-host identity `desktop-wsl` reaches the Arch WSL machine with profile `desktop`.

| Role | Profile | Active tracking entries | Ordinary dotfiles checkout | Mise history HEAD |
| --- | --- | --- | --- | --- |
| Laptop | `algotop` | 105 | `ca8e589b9c39c63a74ac36b90aaf4530495a42ee` | `53c1c9cd2a360e016beb503404f6e2014959bb8c` |
| Desktop / WSL | `desktop` | 84 | `86e383f407dd9a1ff3876d1248f741164de3b8a4` | `53c1c9cd2a360e016beb503404f6e2014959bb8c` |
| Homelab | `archbox` | 84 | `86e383f407dd9a1ff3876d1248f741164de3b8a4` | `53c1c9cd2a360e016beb503404f6e2014959bb8c` |

- Each machine has an ordinary `~/.dotfiles` checkout and a **separate** `~/.local/state/mise/history/repo.git` store. All inspected working trees are clean; each ordinary checkout has one registered worktree.
- All three history stores have local `refs/heads/main` and `refs/remotes/origin/setup` at the current GitHub `master` commit. Local history branch `main` is not a request to rename remote `master`.
- The laptop and homelab ordinary checkouts retain `refs/dots-migrate/pre-cutover-*` refs. Desktop and homelab ordinary checkouts also have stashes. Preserve and inspect these before cleanup; a clean working tree does not mean there is no saved local work.
- GitHub still has `master`, `ArchWSL`, and `niri-config`. A refreshed temporary mirror and redacted Gitleaks scan produced the same six findings recorded in `dotfiles-verification.md`, across 1,507 reachable commits. The current remote snapshot still had zero scanner findings.
- The desktop has an excluded `~/.config/zsh/.secrets` file defining `OPENAI_API_KEY`, with mode **0644**. No value was printed or tested. The file needs owner-only permissions and a deliberate migration; actual cross-user access also depends on directory permissions. The corresponding file is absent on laptop and homelab.

### Watcher-status discrepancy: cause reproduced, released fix verified

Installed mise on all three machines is 2026.9.3. This version stores history locks beneath its cache directory. `sysup mise` and `sysup agents` call `mise cache clear`, which can unlink locks still held by the watcher.

Direct observations:

- Laptop and homelab watchers each hold a deleted cache lock; laptop's held inode differs from the replacement lock inode at the same pathname.
- Both processes remain active, but mise status probes the replacement inode and reports `declared-not-running`.
- Desktop's watcher lock is intact and its status reports `running`.

**Isolated reproduction using installed mise 2026.9.3:** start a watcher in a temporary HOME/state/cache, verify `running`, clear only that temporary cache, then inspect status and process descriptors. Result: watcher remains alive, held locks are deleted, status becomes `declared-not-running`.

**Released fix:** source at mise v2026.9.5 moves history locks into the state directory using `LockFile::at`. A temporary copy of the official 2026.9.5 Linux binary was downloaded and verified against its GitHub release asset SHA-256 digest. The same isolated test kept the watcher `running`, with no deleted held lock, after clearing the temporary cache.

This supports upgrading to the released fix, not inventing a cache-clearing workaround in `sysup`. Before a live upgrade, stop the old watcher and restart it under the new binary so old-cache and new-state lock users cannot overlap. **This investigation itself changed no live binary or service; the subsequently approved live fix is recorded above.**

Sources inspected at their version tags:

- `src/lock_file.rs`
- `src/cli/cache/clear.rs`
- `src/cli/dotfiles/capture_health.rs`
- `src/system/history/watch/runtime.rs`
- `src/system/history/checkpoint.rs`

### Automatic-publication protection: ordinary Git hooks do not work

Both mise 2026.9.3 and 2026.9.5 deliberately override `core.hooksPath` with an empty temporary directory for history-store network operations (`src/git.rs`, `GitPlumbing::network_output`). `src/system/history/sync/publish.rs` and `network.rs` use that path. Setting a pre-push hook in either the ordinary checkout or the history store therefore does not protect automatic publication.

**Executed isolation test on both versions:**

1. Create a temporary HOME/config/state/cache and a disposable local bare remote. Git is limited to the `file` protocol; no real credentials or external remote are available.
2. Install a Gitleaks pre-push hook in the test history repository and add a clearly synthetic, nonfunctional canary matched by an explicit test-only rule.
3. Verify the scanner detects the canary (configured exit 23).
4. Ordinary Git push invokes the hook, fails with exit 1, and leaves the remote unchanged.
5. `mise bootstrap dotfiles watch --once --json` uses the real watcher synchronization path, bypasses the hook, exits 0, and publishes the synthetic canary into the disposable local remote.

The reproduction assertions pass because they establish the **defect in the proposed protection**, not because publication is safe. Task 11's automatic-path protection criterion is **not satisfied**. No transport wrapper, Git shim, post-push scan masquerading as prevention, or replacement synchronization service was introduced.

GitHub's native push protection is a potential server-side alternative that client hook suppression cannot bypass. It protects supported provider token patterns, not arbitrary passwords or private transcripts. Repository API inspection returned `security_and_analysis: null`, so enabled protection cannot be asserted. Algorant subsequently chose this native approach with its documented limits; availability, configured coverage and bypass behavior still require verification before it counts as the Task's prevention control.

Official coverage reference: <https://docs.github.com/en/code-security/reference/secret-security/supported-secret-scanning-patterns>. In particular, GitHub documents that password detections do not support push protection, and legacy token versions may have less protection than current formats.

## Reproducible checks and artifacts

Private investigation directory: `/tmp/dotfiles-remediation.3PrXh9/` (owner-only). Do not publish its repository mirrors or live-derived snapshots.

- `inventory-writers.py` — read-only, value-free inventory, executed locally and via SSH on desktop and homelab; all three runs exit 0. Records refs, registered worktrees, history stores, watcher lock descriptors, and secret-file metadata only.
- `refreshed-scan/safe-summary.json` — refreshed remote snapshot/history findings; scanner exits 0 for the current tree and 10 (configured findings code) for history.
- `probe-mise-boundaries.py` — isolated runtime probes. The resulting scripts and command logs contain only dummy identities and synthetic canaries.
- `/tmp/dotfiles-remediation.3PrXh9/probe-mise-boundaries.py` — exit 0; reproduces the 2026.9.3 cache-lock bug and pre-push bypass. `boundary-results.json` records exact assertions.
- `/tmp/dotfiles-remediation.3PrXh9/probe-mise-boundaries.py --mise /tmp/dotfiles-remediation.3PrXh9/mise-v2026.9.5-linux-x64 --expect-cache-fixed --result-name boundary-results-2026.9.5.json` — exit 0; verifies the released cache-lock fix and confirms pre-push bypass remains. Results are in the named JSON file.
- Each temporary watcher was stopped by the probe's cleanup. No live watcher was stopped, started, or restarted.

## Current boundaries / next steps

1. Revocation confirmation and the approved live safety fixes are complete; historical credential/session material still needs removal.
2. Configure and verify the explicitly chosen native GitHub push-protection scope, including its limitations and bypass behavior. No local hook coverage is claimed.
3. Finalize fnox/Proton Pass migration and headless access, preserving necessary local authentication outside Git. The old Zsh loader is already retired; SecretSpec/Ketch migration has not been performed.
4. Prepare and approve the exact history cleanup/cutover, accounting for stashes, migration refs, all branches, newly created local coordination commits and all three history stores before any remote replacement.
5. Algorant subsequently declared x1nano deprecated and excluded it from the active rollout. It is not a current blocker; if revived, its old checkout must not be pushed into the cleaned repository.
6. Perform post-cleanup fresh-clone scans and approved end-to-end propagation/profile tests before requesting remediation acceptance. Keep one dotfiles repository and keep it private until separately approved for publication.
