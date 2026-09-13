# Dotfiles: pre-README verification

Coordination: `task-1` in the **Algorant GitHub public-readiness** workspace (not the unrelated `task-1` in dotfiles' own workspace).

## Follow-up

Algorant chose a **single public dotfiles repository with secrets outside Git**, not a separate public mirror. Remediation is tracked in `task-11`; see [the current progress report](task-11-progress.md) for restored desktop access, the reproduced watcher-lock issue and its verified released fix, and the automatic-publishing hook limitation. The observations below preserve the initial verification baseline.

## Conclusion

The proposed README narrative is supported by the current configuration, with qualifications below. **Do not make the existing dotfiles repository public yet:** its reachable Git history contains credential material and old agent/session data, despite no Gitleaks findings in the current snapshots.

This was a read-only review. No README, live configuration, repository visibility, credentials, or Git history was changed. No updates, bootstrap applications, synchronization, or pushes were run. Findings contain locations and classifications, never credential values.

## Sources and freshness

- Existing `~/.dotfiles` checkout: `ca8e589b9c39c63a74ac36b90aaf4530495a42ee`, clean but behind GitHub/live configuration. Left untouched.
- Fresh temporary mirror of GitHub: `master` at `53c1c9cd2a360e016beb503404f6e2014959bb8c`; **1,507 reachable commits across all mirrored refs**. Remote branch names include `master`, `ArchWSL`, and `niri-config`.
- A byte snapshot of the laptop's selected live tracking targets was inspected separately.
- The latest remote `sysup`, mise configuration, and Zsh configuration match the laptop's live files. The same three files also match the homelab's live files by SHA-256.
- Audit artifacts are in the owner-only temporary directory `/tmp/dotfiles-verification.POeEwf/`. The mirror and snapshots contain private repository material and must not be published. Only sanitized findings are recorded here.

The root README rewrite must use current facts, not the stale checkout copies. Follow dotfiles' own checkout-update instructions before implementing it; this verification did not pull the checkout.

## Verified README facts

### Three Arch roles

Repository `AGENTS.md` and the `dots` skill describe:

- **Desktop:** Arch under WSL; Windows integration, not a native Linux desktop stack.
- **Laptop:** Arch with Niri and Noctalia.
- **Main homelab machine:** headless Arch server.

Current observations:

| Role | Observation | Boundary |
| --- | --- | --- |
| Laptop | Arch; mise 2026.9.3; selected profile `algotop`; Niri and Noctalia processes running; 105 active tracked entries | Live configuration and tracking targets inspected locally |
| Homelab | Arch; mise 2026.9.3; selected profile `archbox`; `sysup` present; 84 active tracked entries | Read-only SSH through the existing configured `archbox` alias; machine reports hostname `dellmini` |
| Desktop | Documented profile `desktop` and WSL role | The `desktop` SSH name did not resolve during review; not live-verified |

The prose can use generic role names. Actual profile examples must still use the implemented selectors `desktop`, `algotop`, and `archbox`; renaming those is a separate configuration change.

### System updates with sysup

Current script: [`home/.local/bin/sysup`](https://github.com/Algorant/.dotfiles/blob/master/home/.local/bin/sysup), authoritative live path `~/.local/bin/sysup`.

Its default sequence is:

1. `paru -Syu --noconfirm` for system/AUR packages.
2. `mise cache clear`, then upgrade ordinary mise tools.
3. Fast-forward the separate Pi configuration checkout, run its `pi-update` helper, and verify tools.

Routine mise upgrades exclude Rust and the coding-agent group. `sysup rust` updates Rust explicitly; `sysup agents` updates and verifies **Claude Code, Codex, OpenCode, and Copilot** explicitly. The script still depends on the separate Pi checkout/helper; it is not a standalone provisioning solution for arbitrary readers.

This supports “less reliance on AUR,” not “no AUR.” System/desktop packages and custom Niri packaging remain outside mise's user-tool ownership. The repository's existing fresh-machine provisioning Task is deferred.

### Mise tool manifest

Current source: [`config/config.toml`](https://github.com/Algorant/.dotfiles/blob/master/config/config.toml), authoritative live path `~/.config/mise/config.toml`.

There are 23 current tool declarations:

- Runtimes/toolchains: Bun, uv, Node, Rust nightly with `rust-src`.
- Agent/development workflow: Pi, Herdr, Worktrunk, Tandem, Claude Code, Codex, OpenCode, Copilot, Sideshow, Playwright CLI.
- Other tools: zsh-patina, xurl, Ketch, Obscura, croc, flyctl, SecretSpec, Proton Pass CLI, fnox.

Most declarations intentionally follow `latest`; Rust follows `nightly`. The configuration sets `minimum_release_age = "0s"` and uses Bun to install npm-backend tools. A README example should be a clearly labelled representative excerpt, not a claim of pinned reproducibility or the complete manifest.

fnox is **already declared and installed for evaluation** (laptop version 1.35.1). Its declaration explicitly says it has not replaced SecretSpec.

### Mise bootstrap and synchronization

The actual declaration is track-in-place, not Stow or a symlink deployment:

- Live files are edited where applications read them.
- `[settings.history] sync = "sync"` enables automatic two-way sharing.
- `[bootstrap.services.mise-history] builtin = "history-watch"` declares the watcher.
- 105 tracking declarations comprise 84 shared entries plus 21 laptop-profile entries.
- Laptop variants cover Niri, Noctalia, Fuzzel, WirePlumber and related desktop integration. Common CLI/application configuration stays shared.
- Profile selection lives in untracked, machine-local `~/.config/mise/miserc.toml`.
- Saved content appears under `home/`, `home@algotop/`, and `config/` in Git. These are snapshots, not the paths to edit for live application changes.

Official documentation confirms automatic saves, default five-minute publishing and fifteen-minute fetching, credentials required on each machine, and conflict/unsaved-edit pauses. Tool installation, service application, package provisioning, and template rendering are not implied by receiving tracked-file changes.

**Runtime qualification:** on both inspected machines, systemd reports the history service active, while `mise bootstrap dotfiles status --json` reports `declared-not-running`. Status reports no conflicts, pending operations, or sync errors, but `declarations_changed` is true. The laptop watcher process was independently observed running. This discrepancy was not repaired or explained in this review; do not claim an end-to-end healthy three-machine sync test. Matching live files are evidence of alignment, not proof that a new edit propagates automatically today.

### Tool/configuration links for the eventual list

The current tree has inspectable configuration for Atuin, bat, btop, fastfetch, fd, Ghostty, Git, Herdr, lsd, mise, mpv, ncspot, Neovim, paru, SecretSpec declarations, Starship, Tandem, Worktrunk, Yazi, and Zsh under `home/.config/`. Laptop configuration for Fuzzel, Niri, Noctalia and WirePlumber is under `home@algotop/.config/`.

Link actual snapshot files/directories, not retired Stow paths or a claim that every configured application is installed on every machine.

## Publication safety findings

Gitleaks v8.30.1 was downloaded from its official GitHub release and its archive SHA-256 checked against that release's checksums. Scans used the default rules explicitly, ignored inline allow comments, and emitted fully redacted reports. A supplemental current-text assignment check and targeted historical structure inspection were also performed.

| Scope | Result |
| --- | --- |
| Existing checkout HEAD snapshot | 0 scanner findings |
| Fresh remote HEAD snapshot | 0 scanner findings |
| Laptop's selected live tracked regular files | 0 scanner findings; no missing targets |
| All history in fresh GitHub mirror | 6 scanner findings: 5 credential-related occurrences and 1 coordination-identifier false positive |

The tracked `.zshenv` symlink was not dereferenced during snapshot scans; its tracked target `home/.zshenv` was included as an ordinary file. This is a pattern-based assessment, not proof that no secret or private information exists. The desktop's live files and the homelab's full file contents were not secret-scanned.

### Credential-containing historical locations

| Classification | Historical path / line | Commit | Assessment |
| --- | --- | --- | --- |
| OpenAI API key assignment | `zsh/.config/zsh/.zshrc:11` | `ff461e65b794` | Literal `OPENAI_API_KEY` assignment matching provider key format; present in `master` and `niri-config` ancestry |
| Anthropic API key assignment | `zsh/.config/zsh/.zshrc:13` | `140084f58751` | Literal `ANTHROPIC_API_KEY`; present in `master` and `niri-config` ancestry |
| Same Anthropic key in backup | `zsh/.config/zsh/.zshrc.bak:16` | `e29a1d485dec` | Duplicate of the preceding key, not a second distinct Anthropic key |
| Exa API key configuration | `pi/.pi/web-search.json:2` | `2e8d173f81a9` | Literal `exaApiKey` value in old Pi configuration; present in `master` ancestry |
| OpenAI OAuth JWT in agent session | `pi/.pi/agent-sessions/red-team.json:11` | `6fea5b0bdcba` | Decoded only in memory: OpenAI authentication/profile claims, not the common public example token; expiry is in the past. Historical session/privacy exposure remains |

No credential was submitted to a provider. API-key validity and prior revocation are unknown: confirm revocation/rotation before publication rather than assuming old means harmless.

The remaining finding, `pi/.pi/.tandem/papercuts/papercut-15.md:16` at `dc30349d6659`, is a recorded Worker handoff identifier in a coordination incident, not a provider API key.

Additional privacy scope includes historical Zsh history and old agent-session files. The historical `archive/pi/.pi/agent/auth.json` object inspected was an empty JSON object, not an additional credential finding. Existing public-facing identity, location-specific configuration, host information and historical transcripts still deserve deliberate scope review even where scanners are silent.

### Current secrets boundary and fnox

- The current tracked `.zshrc` conditionally sources `$ZDOTDIR/.secrets`; that file is excluded from mise history and Git. It was absent on the inspected laptop and homelab. Exclusions do not erase the old hardcoded keys above.
- The tracked Ketch SecretSpec manifest contains declarations for `BRAVE_API_KEY` and `CONTEXT7_API_KEY`, not values. Its documented backing store is Proton Pass.
- The existing `ketch-sync` workflow writes secrets to Ketch's excluded local configuration. Switching the secret resolver alone does not eliminate an application's plaintext local credential storage.
- There are no encrypted tracking declarations in the current mise manifest.
- Official fnox documentation supports Proton Pass references and explicit `fnox exec -- …` command environments, including use from mise tasks. It recommends explicit wrappers rather than the incomplete experimental mise environment plugin.
- Headless Proton Pass use requires its own authentication/session/key-storage plan. fnox's Proton Pass provider is read-only: creating/rotating vault entries stays with Proton Pass tooling.

## Checks actually run

- `bash -n /home/ivan/.dotfiles/home/.local/bin/sysup` — exit 0 (older checkout).
- `bash /home/ivan/.dotfiles/scripts/sysup/tests/test-sysup-rust-optin.sh` — exit 0, 45 stubbed assertions (older checkout only).
- `bash -n /tmp/dotfiles-verification.POeEwf/remote-scan/head-snapshot/home/.local/bin/sysup` — exit 0 (latest remote version matching live files).
- `bash /tmp/dotfiles-verification.POeEwf/remote-scan/head-snapshot/scripts/sysup/tests/test-sysup-rust-optin.sh` — exit 0, **49 stubbed assertions**, including the four-agent group, update ordering, failure propagation and opt-in Rust behavior. No live upgrades.
- `/tmp/dotfiles-verification.POeEwf/scan.py --repo /tmp/dotfiles-verification.POeEwf/remote.git --output /tmp/dotfiles-verification.POeEwf/remote-scan` — wrapper exit 0; underlying HEAD scanner exit 0, history scanner exit **10** (configured findings code, not a clean result).
- `/tmp/dotfiles-verification.POeEwf/scan-live.py` — exit 0; live scanner exit 0.
- `mise bootstrap dotfiles status --json`, systemd state and process inspection — read-only observations as qualified above.
- Read-only SSH probe using existing `archbox` configuration — exit 0. Initial fully-qualified Tailscale-name attempt failed strict host-key checking; no trust was changed. Desktop-name probe failed DNS resolution (exit 255).
- `fnox --version` — exit 0, 1.35.1 on the laptop.
- `git -C /home/ivan/.dotfiles status --short` — empty at end; checkout HEAD unchanged.

## Decisions before publication

1. Confirm revocation or rotate the exposed OpenAI, Anthropic and Exa API keys; review the historical OAuth/session exposure.
2. Implement Algorant's subsequent single-repository decision through a coordinated history cleanup across all branches, machines and mise history stores. The earlier separate-public-snapshot proposal was not adopted. Do not rewrite only one checkout while other watchers can reintroduce old ancestry.
3. Decide on fnox adoption separately, including headless authentication and the desired command-level exposure of secrets. No plaintext fallback is required. fnox improves future handling; it does not sanitize existing Git history.
4. Resolve or explicitly qualify the watcher-status discrepancy, and verify the desktop when reachable.
5. Write the README from scratch around the agreed three-machine story, current `sysup` behavior, a real mise excerpt, bootstrap synchronization, and linked configuration inventory. No historical migration/fallback narrative needs to be retained.

These are review findings and proposals, not authorization to rotate credentials, change live configuration, rewrite history, create a public repository, or change visibility.

## Official links verified

- [mise dotfiles](https://mise.jdx.dev/dotfiles.html)
- [History and sharing across machines](https://mise.jdx.dev/history.html#sharing-across-machines)
- [Set up a machine with mise](https://mise.jdx.dev/bootstrap/setup.html)
- [fnox](https://fnox.jdx.dev/)
- [How fnox works](https://fnox.jdx.dev/guide/how-it-works)
- [fnox with mise](https://fnox.jdx.dev/guide/mise-integration)
- [fnox Proton Pass provider](https://fnox.jdx.dev/providers/proton-pass)

Current upstream documentation was checked; it is not a substitute for validating installed behavior on each machine. A background documentation helper failed to start; its pane was confirmed to contain only a shell and closed. Documentation verification was completed directly.
