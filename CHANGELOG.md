# Changelog

## 1.2.2

Answers the two functionality notes in the Windhawk catalog's review of 1.2.1.

### Changed

- Chaos Mode's fake crash screen: a plain key now only dismisses it, so Delete no longer removes the selected visual and an arrow key no longer nudges it. A key with Ctrl, Alt or Win still dismisses it and does its usual job (Ctrl+S still saves), and a click still dismisses it.

### Fixed

- Filter map notices Ctrl+Z and Ctrl+Y on every keyboard layout, Cyrillic and Greek included, and also when Ctrl is let go before the Z or Y key comes up.
- Theme check and Filter map find visuals inside groups: a grouped visual's saved position, which is relative to its group, is now read as its place on the page, nested groups included. Stencil keeps grouped blocks where they are, and a shape is matched to its saved file again.

## 1.2.1

Answers the Windhawk catalog's second review of 1.2.0.

### Changed

- Disabling or updating the mod with Power BI open never keeps it loaded. Before, when WebView2 still held one of the mod's handlers, a file call was still running, or a hand-over window was left 15 seconds after a disable, the mod stayed in Power BI until it closed, and an update then loaded a second copy beside it. Now each web view's thread is reached through the mod's own window on that thread, and the disable waits up to two minutes for the rest, then lets Windhawk unload the mod.
- Chaos Mode, the Easter egg, shows a small note at the bottom of the window for as long as it is on: press Esc twice, or type the code again, to leave it.
- The sounds of Chaos Mode and of the Begin-menu programs play only when Skin sounds is on (off by default), like the mod's other sounds.
- Filter map reads the visuals again only after a click or key on the report canvas, in the Filters pane or in the Bookmarks pane, or an undo or redo (Ctrl+Z, Ctrl+Y, Power BI's Undo and Redo buttons), instead of after any click anywhere. The ribbon, the Format, Visualizations, Fields and Selection panes and saving no longer start a pass. Changes in the Filters pane, and new files after a save, still refresh it.
- The readme describes Chaos Mode as a mode that stays on until you leave it, says how to leave it, mentions its crash screen on pages with pie or donut charts, and says its sounds follow Skin sounds. "What it reads and keeps" lists every file the Stencil frames script writes and no longer says the Stencil script never overwrites a file that exists. The Skin sounds and Hidden surprises settings and the help say the same.

### Fixed

- Badge cards in Report view pin on a click again. Power BI's Report view page has no PointerEvent constructor, so the click threw before the card opened.
- Chaos Mode's fake crash screen no longer swallows the key that dismisses it, so Ctrl+S still saves.
- Disabling the mod during an Interactions "set all" run ends the run, and no bar or colored icons come back.
- Disabling the mod during a Filter map run across every page no longer switches back to your page or shows a toast afterwards.
- Disabling the mod while Stencil waits for a fresh save to be read no longer builds, copies the script or shows a toast afterwards.

## 1.2.0

The first release for the Windhawk catalog. It holds every change since 1.0.2; 1.0.3 and 1.1.0 were never released on their own.

### New

- The tools find the open report by themselves when it is saved as a Power BI project (.pbip): the report Power BI was started with, then any report it opens, and again after each save. Theme check, the theme palette in Colors, Filter map and Stencil compare with what was just saved. The "Report project folder" setting is now only a fallback for a window where no .pbip was opened, and a change to it reaches open windows at once.
- Save As to a new folder is followed. The tools switch to the new report instead of reading the old one.
- Stencil saves templates (Build menu), starts a page from a searchable list of layouts and your templates, and keeps groups of blocks together. Blocks are drawn by dragging, 28 more visual types are in a menu, and Ctrl+C, Ctrl+X and Ctrl+V work inside Stencil only. Convert to visuals sits on the strip.
- Stencil can draw card frames as the page's background image (Convert to background, or the "with frames as background" switch in Build). A build asked for just after a save waits for the saved report to be read instead of failing.
- Classic has two styles, Clean and Power BI 95 (silver panes, heavy bevels, a teal desktop and a taskbar with a clock), picked beside the Skins gallery.
- A new "Hidden surprises" setting, on by default. It covers an Easter egg and the Begin menu in the Power BI 95 style. Turn it off and both are gone, along with their key listener. Neither changes the report.

### Changed

- Disabling or updating the mod with Power BI open now unloads it cleanly instead of keeping it loaded until Power BI closes.
- Filter map costs less while it is on, ignores typing in text fields, and the badge words open in a panel within the visual's width. Interactions' bar shows progress and the result of a run across all visuals.
- Badge cards and the menu no longer flicker. A card has a line saying what it counts, and Colors shows a swatch beside the nearest palette color.
- The Add data screen of an empty report keeps Power BI's own colors under every skin.
- The Power BI 95 look follows "Keep the report's Filters pane colors".
- The readme, settings and help say to restart Power BI after enabling, updating or changing the mod's settings, and describe more exactly which tools press Power BI's own buttons and which files are read.
- 64-bit only, matching Power BI Desktop.

### Fixed

- Hotkeys leave typing alone: in a text box, the formula bar, DAX query view or TMDL view, Ctrl+Alt+[ and ] are left for typing, which matters on keyboards that type [ and ] with AltGr (German, French, Nordic, Czech and more). Letter hotkeys also work on Cyrillic, Greek and Polish layouts.
- Changing a mod setting no longer deletes Stencil blocks, and a failed save now shows one warning.
- A report project folder under OneDrive or a synced SharePoint library is read in full, with junctions and folder links skipped. A .pbip whose report folder has accents or another script now works.
- Disabling the mod puts Power BI's tab underline back and stops every timer the tools started.
- A bulk run in Filter map across pages stops with a warning when a page does not open in time.
- The menu closes properly when it was opened with Ctrl+Alt+K in a view without a status bar.
- Stencil counts a block as built only when the visual under it is of the block's type, so a pie block over a column chart is no longer skipped by Convert or removed by Clear built.

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
