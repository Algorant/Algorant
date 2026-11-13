---
id: task-21
uid: e99c2f1f-6e14-46bf-875c-997f96f88c04
type: task
title: "Review verdigris against the readiness bar and correct its card"
state: todo
priority: "high"
effort: "medium"
references: ["Algorant/verdigris", "Algorant/omarchy-verdigris-theme"]
tags: ["portfolio", "verdigris", "review"]
accord:
  status: "ready"
  acceptance: ["Every app page is checked against the repo itself: theme file, screenshot currency, README install line and working links", "The five readiness items are each marked met or not met with evidence at the current tip", "task-4 is rewritten to the verified state, with an owner named for each remaining gap", "One screen reaches Herdra: whether verdigris is done, and what is genuinely left"]
  updatedAt: "2026-11-13T04:35:04Z"
createdAt: "2026-11-13T04:35:04Z"
updatedAt: "2026-11-13T04:35:04Z"
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
