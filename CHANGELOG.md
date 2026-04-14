# Changelog

All notable changes to VolumeBoost will be documented in this file.

The format follows Keep a Changelog and uses semantic versions for shipped builds.

## [1.0.1] - 2026-04-14

Polish update for the direct-download beta release track.

### Added

- Live Sparkle feed publishing through GitHub Pages for direct-download updates.

### Changed

- Refreshed the app icon and menu bar glyph with the approved modern branding.
- Simplified the menu bar popover into a cleaner primary action row and compact utility footer.
- Kept public release archives on the marketing version name instead of exposing internal build numbers in the download filename.

### Fixed

- Startup hangs that could leave the app stuck in the orange `Starting...` state until relaunch.
- Popover activation, inline help, update-button visibility, and footer alignment issues discovered during beta testing.

## [1.0.0] - 2026-04-14

Initial direct-download beta release.

### Added

- Native menu bar app for boosting quiet system audio on macOS 14.2+ using Core Audio taps.
- Manual boost slider with smart boost and soft limiter controls.
- Launch-at-login support for the packaged app.
- Notarized direct-download packaging with signed zip artifacts and checksums.
- Lightweight diagnostics with local breadcrumb logging and exportable support bundles.
- Release packaging scripts for app bundles, zips, notarization, and checksums.
- Vendored Sparkle framework and publishing helpers for `generate_keys`, `generate_appcast`, and beta release packaging.
- Dedicated beta release page at `release-notes/beta/index.html`.

### Changed

- Replaced the old capture-and-replay prototype path with the Core Audio taps shipping path.
- Moved the release bundle build to the Xcode `VolumeBoostApp` target.

### Fixed

- Repeated start/stop startup hangs that could leave the app stuck in the orange `Starting...` state.
- Initial inactive popover rendering that made controls hard to read on first click.

### Notes

- Automatic updates are now integrated into the direct-download track, but the updater UI remains hidden until a real hosted appcast feed URL and public Ed25519 key are configured for the packaged build.
