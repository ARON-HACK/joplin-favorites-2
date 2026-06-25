# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.6.0] - 2026-06-25

### Added

- Marketplace metadata: `categories` (`productivity`, `personal knowledge management`) and `screenshots` in the plugin manifest for a richer listing on the Joplin plugin marketplace

### Changed

- Panel preferences (drag & drop, panel title, type icons, line height, widths, fonts, colors) are now stored in Joplin's `settings.json` (`SettingStorage.File`) instead of the database, so they can be carried across installations by copying the settings file. Favorites themselves remain in the database to avoid data loss on upgrade (Joplin has no DB→file migration for an existing setting key)

## [1.5.0] - 2026-06-25

### Added

- Quick jump keyboard shortcuts (`Cmd+1`~`9` on macOS, `Ctrl+1`~`9` on Windows/Linux) to jump to the first 9 favorite items
  - Works for all favorite types (notebooks, notes, to-dos, tags, searches)
  - Shortcuts are pre-configured and can be customized in `Tools > Options > Keyboard Shortcuts`
- Default accelerator `Cmd/Ctrl+Alt+F` for the toggle panel visibility command

### Changed

- Renamed plugin display name to `Favorites 2`

## [1.4.0] - 2026-06-22

### Changed

- Project forked and now maintained by [ARON-HACK](https://github.com/ARON-HACK/joplin-favorites-2)
- New plugin id (`hack.aron.joplin.favorites`) and npm package (`joplin-plugin-aronhack-favorites`) so it can be published independently to the Joplin marketplace
- Updated author, homepage, and repository metadata

## [1.3.2] - 2023-11-19

### Fixed

- Plugin version in `manifest.json`

## [1.3.1] - 2023-11-19

### Fixed

- Opening a favorited item often doesn't work with Electron 26 ([#26](https://github.com/benji300/joplin-favorites/issues/26) by [@personalizedrefrigerator](https://github.com/personalizedrefrigerator))

## [1.3.0] - 2021-08-12

### Changed

- Updated plugin API to version v1.8.2 (`registerSettings`) to support app version v2.2.4 or newer
- Do not trim search queries (whitespaces before or after won't be removed)

### Removed

- Bundled font packages (FontAwesome, Roboto)
  - Use built-in versions to decrease plugin size
- External `copy-to-clipboard` package
  - Use of clipboard functionality provided by plugin API v2.1.5

## [1.2.1] - 2021-02-23

### Fixed

- Issue that caused infinite message loop between plugin and app ([#7](https://github.com/benji300/joplin-favorites/issues/7))
- Ability to drag note favorites onto [note-tabs plugin](https://github.com/benji300/joplin-favorites) panel

## [1.2.0] - 2021-02-17

### Added

- Ability to drag & drop notes from [note-tabs plugin](https://github.com/benji300/joplin-favorites) to add as favorite
- Ability to rename and delete favorites directly in panel (vertical layout only)
  - Via new hover buttons on the right side

### Changed

- Drag & drop behavior to add notebooks, notes or to-dos
  - Move them onto the panel to add new favorite at the dropped position
- Scroll horizontally without holding `Shift` key
- Plugin command labels (Removed `Favs:` prefix)

### Fixed

- Search favorites with phrases in query cannot be opened, edited or deleted ([#4](https://github.com/benji300/joplin-favorites/issues/4))

## [1.1.0] - 2021-01-21

### Changed

- Improve style of scrollbar in vertical layout

### Fixed

- Edited search queries not saved
- Reduced opactiy of dragging favorite

## [1.0.0] - 2020-01-18

- Initial Release
