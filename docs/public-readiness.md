# Public-readiness map

This file maps each portfolio project to its repositories, its local checkout, and how its public version is produced. The order and the readiness bar are in [VISION.md](../VISION.md). **Live state and next steps live on the Tandem board, one card per repo**; this map is the stable reference: identity, visibility and mechanism.

Baseline visibility was checked on 2026-10-11; pi's flip (2026-11-10), tandem 0.17.7 (2026-11-11) and verdigris's rescope (2026-11-12) were verified then. Re-check before relying on it.

| Order / Board card | Project | Public repository | Private source | Checkout | Visibility | Public version produced by |
|---|---|---|---|---|---|---|
| 1 | pi setup | [Algorant/pi](https://github.com/Algorant/pi) | `Algorant/.pi` | `~/.pi` | **Public** (flipped 2026-11-10, fresh history) | "Publish pi snapshot" Action on every `main` push of `.pi` |
| 2 | tandem | [Algorant/tandem](https://github.com/Algorant/tandem) | (same) | `~/Projects/tandem` | Public, 0.17.7 | direct; site via GitHub Pages |
| 3 | verdigris | [Algorant/verdigris](https://github.com/Algorant/verdigris) and [Algorant/omarchy-verdigris-theme](https://github.com/Algorant/omarchy-verdigris-theme) | (same) | `~/Projects/verdigris` | Public (palette/ports fresh history since 2026-10-26; old history private in `Algorant/verdigris-archive`) | direct; theme installs via `omarchy theme install` |
| 4 | dotfiles | [Algorant/dotfiles](https://github.com/Algorant/dotfiles) | `Algorant/.dotfiles`, `omarchy` branch | none (mise history) | Private; public direction approved 2026-11-12, actual flip still pending | on-demand publisher in private `Algorant/.algOS` (checkout `~/.algOS`; owner: algOS Ceph) |
| 5 | algOS showroom — a tailored Omarchy/Arch setup | [Algorant/algOS](https://github.com/Algorant/algOS) (prepared in private `omarchy-setup`) | `Algorant/.algOS` (private operations, installer, VM proof, publisher) | `~/Projects/omarchy-setup`; ops checkout `~/.algOS` | **Public** (2026-11-16, fresh history `00d2c65`); ops private | direct, fresh-history showroom; installer stays private in `.algOS` |
| 6 | herdra | [Algorant/herdra](https://github.com/Algorant/herdra), with [herdr-agent-tree](https://github.com/Algorant/herdr-agent-tree) (public) and [herdr-notifs-plus](https://github.com/Algorant/herdr-notifs-plus) (private) | (same) | `~/Projects/herdra` | Private; stays private until Algorant raises it | not decided, and not a pending decision |
| parked | side projects | [mediafetch](https://github.com/Algorant/mediafetch) (private) | obsmd `Algorant/obsmd`, finanza `Algorant/finanza` | `~/Projects/{obsmd,finanza,mediafetch}` | mediafetch private; obsmd private by decision (2026-10-26); finanza private | not this board's work unless Algorant says otherwise |
| parked | older profile projects | xunfurl, RSSify, retrokit, AlgoPDF | (same) | — | unchanged since 2026-10 | same |

Full algOS cutover landed 2026-11-14, superseding the earlier algomarchy/.algomarchy name lock: private `Algorant/.algOS`, checkout `~/.algOS`, algOS Ceph; future public `Algorant/algOS`. Mixed case is explicitly approved. Framing: a tailored Omarchy/Arch setup, not an operating system. `algomarchy-bootstrap` was folded into private operations and archived. The profile README links `Algorant/algOS` since the 2026-11-16 flip, as Algorant asked. dotfiles remains dotfiles and stays private by his decision (2026-11-15): "leave dotfiles private. the links can just be dead for now".

Visibility and readiness are not permission: nothing flips without Algorant's explicit OK for that specific repository, at that moment. Approving readiness never authorizes pushing, rewriting history or changing visibility. AlgoNix was dropped from the profile on 2026-10-11 in favour of Algomarchy.

## Review checklist

To bring a project to its shippable bar ([AGENTS.md](../AGENTS.md)), its own Ceph:

1. Checks the tracked tree and Git history for secrets, private data, and machine-local state, and records locations without copying values. A clean tree does not prove a clean history.
2. Checks the README against `repo-style-rules`: banner, first person, succinct, `[MIT](LICENSE)` last.
3. Checks licensing and attribution, including derived work (for example, AlgoPDF's NightPDF base).
4. Validates with the project's own commands and records any gaps.
5. Confirms the private→public mechanism works repeatably (a flip, or a generator run and its diff).
6. Gets Algorant's decision. Approving readiness does not authorize pushing, rewriting history, or changing visibility.

## Adding a project

Confirm its GitHub identity and its place in the order with Algorant. Match checkouts by Git remote, not directory name. Then add a card and a row here. Adding a project to this map does not give permission to publish it.
