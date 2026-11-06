# Changelog

## 1.0.2

- Stencil's build script carries the project folder inside its encoded data, so no folder name can be read as PowerShell code, whatever quotes it contains.
- Stencil's Build accepts a project folder typed with backslashes, the way Explorer copies paths.
- The menu and the help panel credit the mod's author.

## 1.0.1

- New license: CC BY-ND 4.0. Use it, at work too, and share unchanged copies with credit;
  modified or rebranded versions may not be shared. 1.0.0 was released under the MIT License.
- The mod's readme in Windhawk states the license.

## 1.0.0

The first public release.

- 13 skins for the whole Power BI Desktop window, every view and dialog included: Blue Hills,
  Classic Grey, Stronghold, Gunmetal Console, Hazard Suit, Analytic Endeavors, Starship Panel,
  Phosphor Terminal, Neon Grid, High Contrast Ink, Graph Paper, Midnight Orchid and Arctic Frost.
  Pick one from the Skins group on the View ribbon, the status bar chip or Ctrl+Alt+K. None puts
  Power BI back as it was. Skins never change the report page or its visuals.
- Tools for report authors:
  - Stencil: draw a page layout as see-through blocks, then copy a PowerShell script that builds
    them as real visuals in the report project folder (new files only).
  - Layout QA: a grid, rulers and a label on every visual, with marks for edges and gaps that are
    a few pixels off.
  - Filter map: each visual's visual, page and report filters and its slicers and cross-filters,
    plus a menu to hide, show, lock or unlock visual-level filters in bulk.
  - Theme check: visuals whose saved formatting differs from the report theme.
  - Colors: text, bars, lines and points that are hard to read (WCAG AA or AAA), and colors off
    the palette.
  - Interactions: colored icons in Edit interactions and a bar that sets every other visual to
    None, Filter or Highlight at once.
- A help page (Ctrl+Alt+H) with what every mark means, every key and every setting.
- Extras, each a switch in the menu: a splash when a skin is picked, short notes on visual errors
  and finished refreshes, confetti when a refresh finishes, skin sounds (off by default), the
  visual count in the status bar, and an optional sound file of your own for the confetti.
- Works with Power BI's light and dark modes. Runs locally, makes no network requests, and reads
  files only for the report project folder and sound file settings.
