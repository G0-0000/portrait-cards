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
- **Gallery:** this repo carries the `herdr-layout` topic, so it appears at
  herdr.dev/layouts.

`spaces-cards` and `agents-cards` are derived from Herdr's shipped `spaces`
and `agents` mods under the Apache License 2.0; see [NOTICE](NOTICE) and
[LICENSE-Herdr.txt](LICENSE-Herdr.txt).
