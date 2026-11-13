# portrait-cards

A portrait-friendly layout for the [Herdr](https://herdr.dev) desktop app:
horizontal project cards across the top, horizontal agent cards across the
bottom, and one large terminal between them. Active cards are transparent with
a 4px blue bar — on top for projects, on the bottom for agents.

![portrait-cards](preview.png)

- **Recipe:** [RECIPE.md](RECIPE.md) — the brief for rebuilding it from an
  empty folder.
- **Install:** copy `layouts/portrait-cards.json` into
  `~/.config/herdr-app/layouts/`, `mods/spaces-cards/` and
  `mods/agents-cards/` into `~/.config/herdr-app/mods/`,
  `themes/ghostty-mocha.json` into `~/.config/herdr-app/themes/`, merge
  `keys.json` into your own, then
  `herdr-app do layout.switch --name portrait-cards`. Never overwrite a name
  you already have.
- **Keys:** `⌘↑ ⌘↓ ⌘← ⌘→` all step through agents. They are bound in three
  sections of `keys.json` (`global`, `terminal`, `layout:portrait-cards`)
  because `terminal` outranks `global`. As a side effect the terminal no longer
  receives `⌘←` / `⌘→` for beginning/end of line — Ctrl-A / Ctrl-E still work,
  or drop those two keys from `terminal` to keep it.
- **Trackpad swiping is not included.** Herdr turns a two-finger horizontal
  swipe into a `MouseDown(Navigate)` event, which neither `keys.json` nor a mod
  can read (the mod bridge reports it as `"left"`), so a swipe gesture needs a
  system-level listener outside Herdr. Upstream request:
  [herdr-app#249](https://github.com/herdrdev/herdr-app/issues/249).
- **Gallery:** this repo carries the `herdr-layout` topic, so it appears at
  herdr.dev/layouts.

`spaces-cards` and `agents-cards` are derived from Herdr's shipped `spaces`
and `agents` mods under the Apache License 2.0; see [NOTICE](NOTICE) and
[LICENSE-Herdr.txt](LICENSE-Herdr.txt).
