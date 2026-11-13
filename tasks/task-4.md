---
id: task-4
uid: 65bf0b8b-f1b6-45e8-b6eb-028665166e14
type: task
title: "verdigris: public colour scheme repo (rescoping with its Ceph)"
state: todo
references: ["https://github.com/Algorant/verdigris", "https://github.com/Algorant/omarchy-verdigris-theme", "https://github.com/Algorant/verdigris.nvim"]
tags: ["public-readiness", "verdigris"]
accord:
  status: "ready"
  acceptance: ["The project meets the shippable bar in AGENTS.md; verified independently here from a fresh anonymous view.", "Every profile or channel link to it resolves for an anonymous visitor.", "Algorant's decision to publish (or to defer) is recorded."]
  constraints: ["Each project's own Ceph makes its changes; this workspace records state and asks through Herdra.", "Do not push other repositories, change visibility, rewrite history, or publish without Algorant's explicit word.", "Nothing private in this public board: no credentials or personal records (family, home address, financial or health data, private correspondence, vault content)."]
  updatedAt: "2026-10-29T03:13:37Z"
createdAt: "2026-09-12T03:58:08Z"
updatedAt: "2026-11-13T04:37:14Z"
priority: "high"
---
## State — verified in the repo at `55ad1e7` (2026-11-13), not from reports

**Goal (Algorant's words, 2026-11-12):** a public colour scheme repo where people can see what he uses for config, with pictures and demos of what it looks like for every piece of software — modelled on kepano's flexoki: a palette, a real theme file, and a screenshot per supported app.

Both repos are public: `Algorant/verdigris` (fresh history since 2026-10-26, 178 tracked files) and `Algorant/omarchy-verdigris-theme` (2026-10-15). Old history stays private in `verdigris-archive`.

What the repo actually contains today:
- `palette/` — `verdigris.json` (version 0.2.0), `verdigris.css`, `notes.md`, README.
- `docs/` — `banner.png`, `banner.svg`, `palette-swatch.svg`, thumbnails.
- `apps/` — **19 folders** (atuin, btop, eza, fastfetch, flea, ghostty, herdr, hokum, lazygit, leaf, nvim, obsidian, omarchy, pi, spotifast, starship, tandem, yazi, zsh), every one with a README, at least one screenshot and thumbnails.
- `CHANGELOG.md` at 0.2.0 (2026-11-06), `LICENSE` (MIT, GitHub agrees), `build/`.

## Five readiness items at the current tip

1. **README — met, with three blemishes.** Banner as the title (no H1), palette swatch, a gallery of nine screenshots plus six more, grouped lists (os / terminal-cli / apps), a "how to use" line, and `## License` with `[MIT](LICENSE)` last; no trailing full stops. Blemishes: line 8's `[additional colors]` is a reference with no target, the tone is imperative rather than first person, and two of its outbound links 404 (below).
2. **MIT — met.** `LICENSE` at the root, GitHub reports MIT.
3. **gitguard — met for the repo, with a scan gap.** Enabled, fleet config, hooks fire on every push (pre-push records 2026-11-13). The last **full-history** pass was at `6aa49f7` (22 commits, 0 findings); the rescope commits after it (`a6c5683`, `be23bff`, `4bc1fcf`, `53b9a6a`, `5d3ed95`, `55ad1e7`) have only incremental coverage.
4. **Current — met.** Commits on 2026-11-12 and 2026-11-13; every app's screenshots were retaken in this rescope (all 19 app folders last touched 2026-11-12), so none is stale against palette 0.2.0.
5. **Mechanism — n/a.** Public since 2026-10-26; no generator, no flip pending.

## Per-app goal

- 16 of 19 apps ship a real theme file in the app's own format (`atuin`, `btop`, `eza`, `fastfetch`, `ghostty`, `herdr`, `hokum`, `lazygit`, `leaf`, `obsidian`, `omarchy` (4 sub-areas), `pi`, `starship`, `tandem`, `yazi`, `zsh`).
- Three ship none, and two say why: **flea** takes its colors from the omarchy theme, **nvim** keeps its colorscheme in the public `Algorant/verdigris.nvim`. **spotifast** has screenshots and no explanation at all.
- Links: 0 broken relative links; **2 dead external links** — `Algorant/hokum` (404) and `Algorant/omarchy-setup` (404 while the guide is private).

## Gaps and their owners

| Gap | Owner |
|---|---|
| `[additional colors]` reference with no target in README line 8 | verdigris Ceph |
| `Algorant/hokum` 404 — publish the repo or drop the link | verdigris Ceph, with Algorant if publishing hokum is the answer |
| spotifast page: no theme file and no note on where its colors come from | verdigris Ceph |
| Full-history gitguard pass after the rescope commits | verdigris Ceph (or the gitguard Ceph) |
| No git tags or GitHub releases for a palette now at 0.2.0; `CHANGELOG` still cites bat and Windows Terminal pages that no longer exist and claims every theme file states its palette version (2 of 19 do) | verdigris Ceph |
| `Algorant/omarchy-setup` 404 resolves when the guide flips | dotfiles + guide cards (his flip word) |

## Next step

Nothing here waits on Algorant. The verdigris Ceph closes the six gaps above; this card re-verifies when it reports.