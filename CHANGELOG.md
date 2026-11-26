# MovieBrowser – Changelog

All notable changes to MovieBrowser are documented in this file.

## [4.3] - 2026

### Added
- Added TMDb Discover integration for movies and TV series.
- Added new language translations.
- Added automatic update functionality.
- Added optional background overlay for Discover:
  - Off
  - Light
  - Medium
  - Dark

### Improved
- Improved visual text presentation.
- Removed all remaining TheTVDb references and dependencies.

### Fixed
- Fixed database reset functionality.

---

## [4.2] - November 2026

### Added
- New plugin logo (`plugin.png`).
- New movie selection frame.

### Fixed
- Reworked screen layouts and fixed display issues.
- Fixed series information display.
- Fixed MovieBrowser player closing with the EXIT button.
- Fixed library.py: series information and covers now use TMDb instead of TheTVDb.
- Fixed library scanning and filename recognition to prevent duplicate movie entries.
- Fixed TMDb search title filtering, which previously truncated movie titles after the first word.
- Fixed background and default poster loading.
- Fixed blacklist reading errors.
- Updated German (DE), Italian (IT) and Dutch (NL) translations.

---

## [2025-12-02] - Major Rewrite

### Changed
- Completely recoded MovieBrowser.
- Reworked the entire database implementation.
- Rewrote screen layouts and interface components.
- Updated source code and API URLs.
- Separated libraries into dedicated modules.
- Introduced the new TMDb API v4.

### Fixed
- Fixed MovieList banner display.
- Removed unused and unnecessary code.

---

## Development History

### [2025-05-16]
**Lululla**
- Refactored all classes.
- Cleaned up unnecessary code throughout the plugin.

### [2024-09-20]
**Lululla**
- Recoded and cleaned up the plugin.
- Removed unnecessary code.

### [2022-12-22]
**Lululla**
- Major code rewrite.
- General fixes and improvements.

### [2022-12-08]
**Lululla**
- Added `callInThread`.
- Added `getMountDefault`.

### [2022-12-04]
**Lululla**
- Added language support.
- Added configuration improvements.
- Major bug fixes.

### [2022-10-04]
**Kiddac**
- Added Python 3 compatibility.
- Various code improvements and fixes.
