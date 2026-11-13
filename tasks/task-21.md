---
id: task-21
uid: e99c2f1f-6e14-46bf-875c-997f96f88c04
type: task
title: "Review verdigris against the readiness bar and correct its card"
state: "in-progress"
priority: "high"
effort: "medium"
references: ["Algorant/verdigris", "Algorant/omarchy-verdigris-theme"]
tags: ["portfolio", "verdigris", "review"]
accord:
  status: "delivered"
  acceptance: ["Every app page is checked against the repo itself: theme file, screenshot currency, README install line and working links", "The five readiness items are each marked met or not met with evidence at the current tip", "task-4 is rewritten to the verified state, with an owner named for each remaining gap", "One screen reaches Herdra: whether verdigris is done, and what is genuinely left"]
  claimedAt: "2026-11-13T04:37:11Z"
  deliveredAt: "2026-11-13T04:37:22Z"
  summary: "Reviewed verdigris in the repo at 55ad1e7 rather than from reports: five readiness items marked with evidence, all 19 app pages checked, links and screenshots verified. Verdigris is substantially done; six small gaps remain, all owned by its Ceph except the guide link that resolves with his flip."
  evidence: ["178 tracked files at 55ad1e7; palette/ (verdigris.json v0.2.0, css, notes), docs/ (banner.png/svg, palette-swatch.svg, thumbs), apps/ with 19 folders, CHANGELOG 0.2.0, MIT", "19 app folders each with README + screenshot(s) + thumbs; 16 have a theme file; flea takes omarchy colors, nvim's colorscheme lives in public Algorant/verdigris.nvim, spotifast unexplained", "0 broken relative links; 2 dead external links (Algorant/hokum 404, Algorant/omarchy-setup 404) and one reference with no target ([additional colors], README:8)", "All 19 app folders last touched 2026-11-12: screenshots retaken, none stale against palette 0.2.0", "gitguard enabled with hooks firing 2026-11-13; last full-history pass at 6aa49f7 (22 commits, 0 findings), no full pass since the rescope commits", "task-4 rewritten with the verified state, a gap table naming an owner per gap, and nothing waiting on Algorant"]
  updatedAt: "2026-11-13T04:37:22Z"
createdAt: "2026-11-13T04:35:04Z"
updatedAt: "2026-11-13T04:37:22Z"
assignee: "algorant"
---

## Description

Algorant (2026-11-13): "lets do an actual review of verdigris as a task a lot of that we actually did do"

The card (`task-4`) says the rescope is still being planned and that the card records state only, so the board reads as though the palette, theme files and screenshots are ahead of us. They are not: much of it is already in `~/Projects/verdigris` (indexed 2026-11-13):

- `palette/` with `verdigris.css`, `verdigris.json` and `notes.md`.
- 19 app folders, every one with a `README.md`, at least one `screenshot.png` and thumbnails: atuin, btop, eza, fastfetch, flea, ghostty, herdr, hokum, lazygit, leaf, nvim, obsidian, omarchy, pi, spotifast, starship, tandem, yazi, zsh.
- A theme file in most of them; `flea`, `nvim` and `spotifast` carry none.
- `docs/banner.svg/png`, `docs/palette-swatch.svg`, per-app chips in `docs/thumbs/`, MIT `LICENSE`, gitguard config.
- 178 tracked files; today's commits include Hyprland borders from the generated theme, ANSI slot 7, American spelling.

What is not established is whether that adds up to the bar, and the card does not say.

Review, from the repo as it is now (not from memory, and not from the last report):

1. All five readiness items, each met or not with the evidence: README in his `repo-style-rules`, plain MIT, gitguard passed at the current tip, content current with the work, and the private-to-public mechanism verified.
2. The rescope goal in his words ("a palette, a real theme file and a screenshot per supported app, plus the Omarchy theme"): per app, what ships and what does not.
3. The three apps with no theme file, and anything a stranger would hit: dead links, stale screenshots, pages with no install line.
4. Rewrite `task-4` so it states what is true and what is genuinely left, with an owner on each gap, and keeping the "records state only" rule.

Report to Herdra: one screen — verdigris done or not, and the short list of what remains.
