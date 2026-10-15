# Public-readiness map

This file maps each portfolio project to its repositories, local checkout, and how its public version is produced. Each project's state, crippling issues, and next step live in its Task on this board ([AGENTS.md](../AGENTS.md)). The aims and order are in [VISION.md](../VISION.md).

Baseline visibility was checked on 2026-10-11 with `gh repo view`; Verdigris's two repositories, generated dotfiles and omarchy-setup were rechecked on 2026-10-15. Re-check before relying on it.

| Order / Task | Project | Public repository | Private source | Checkout | Visibility | Public version produced by |
|---|---|---|---|---|---|---|
| 1 / `task-4` | Verdigris | [Algorant/verdigris](https://github.com/Algorant/verdigris) and [Algorant/omarchy-verdigris-theme](https://github.com/Algorant/omarchy-verdigris-theme) (Omarchy port, public 2026-10-15) | (same) | `~/Projects/verdigris` (palette/ports) | Private (palette/ports) / Public (Omarchy theme) | direct; theme installs independently via `omarchy theme install` |
| 2 / `task-3` | Tandem | [Algorant/tandem](https://github.com/Algorant/tandem) | (same) | `~/Projects/tandem` | Public | direct; site via GitHub Pages |
| 3 / `task-2` | Pi setup | [Algorant/pi](https://github.com/Algorant/pi) | `Algorant/.pi` | `~/.pi` | Private (generated) / Private (source) | "Publish Pi snapshot" Action on every `main` push |
| 4 / `task-12` | Dotfiles | [Algorant/dotfiles](https://github.com/Algorant/dotfiles) | `Algorant/.dotfiles`, `omarchy` branch | none (mise history) | Private pending omarchy-setup VM proof and Algorant's approval (generated) / Private (source) | on-demand publisher in private Algorant/Algomarchy reading `.dotfiles@omarchy` (Algomarchy task-69); replaces the old `master`-triggered Action |
| 5 / `task-13` | Algomarchy guide | not yet decided (profile links [Algorant/Algomarchy](https://github.com/Algorant/Algomarchy)) | `Algorant/Algomarchy` | `~/Projects/Algomarchy` | Private | not yet decided |
| 6 / `task-14` | obsmd | `Algorant/obsmd` or a public subset | `Algorant/obsmd` | `~/Projects/obsmd` | Private | not yet decided |
| 7 / `task-9` | mediafetch | [Algorant/mediafetch](https://github.com/Algorant/mediafetch) | (same) | `~/Projects/mediafetch` | Private | direct |
| 8 / `task-15` | finanza rulebook | not yet decided | `Algorant/finanza` | `~/Projects/finanza` | Private | written fresh; no source is published |

Not in current focus (still linked from the profile): xunfurl (`task-6`), RSSify (`task-7`), retrokit (`task-8`), AlgoPDF (`task-10`). AlgoNix was dropped from the profile on 2026-10-11 in favour of Algomarchy.

The public Omarchy theme is separate from `Algorant/omarchy-setup` and generated `Algorant/dotfiles`: both setup repositories remain private, with publication gated on VM proof (Herdra update, 2026-10-15). The private `Algorant/.pi` source is optional and never cloned as part of that setup.

## Review checklist

To bring a project to its shippable bar ([AGENTS.md](../AGENTS.md)), its own Ceph:

1. Checks the tracked tree and Git history for secrets, private data, and machine-local state, and records locations without copying values. A clean tree does not prove a clean history.
2. Checks the README's promises against the implementation, and states the work-in-progress status and known issues.
3. Checks licensing and attribution, including derived work (for example, AlgoPDF's NightPDF base).
4. Validates with the project's own commands and records any gaps.
5. Gets Algorant's decision. Approving readiness does not authorize pushing, rewriting history, or changing visibility.

## Adding a project

Confirm its GitHub identity and its place in the order with Algorant. Match checkouts by Git remote, not directory name. Then add a Task and a row here. Adding a project to this map does not give permission to publish it.
