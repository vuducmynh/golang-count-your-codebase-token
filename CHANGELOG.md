# Changelog

All notable changes are documented here. CodeDocs follows semantic versioning.

## [Unreleased]

## [1.8.5] - 2026-10-13

### Added

- Multi-segment path suffix matching in scanner so nested paths like `heygoru/references` are excluded regardless of whether the scan starts at the project root or a parent directory.
- Expanded Rust and Electron desktop build exclusions: unpacked desktop output directories (`win-unpacked`, `mac-unpacked`, `linux-unpacked`, `dist-electron`, `dist_native`, `app-builds`), native C++/Cargo build caches (`cmake-build-*`, `vcpkg_installed`, `.cargo/registry`, `.cargo/git`), electron-builder metadata (`latest*.yml`, `builder-effective-config.yaml`), and binary extensions (`.wasm`, `.iobj`, `.ipdb`, `.pch`, `.gch`, `.idb`, `.tlog`, `.def`, `.imp`, `.res`, `.syso`, `.tlb`, `.profraw`, `.profdata`, `.pgd`, `.pgc`, `.dat`, `.dmp`, `.mdmp`, `.hdmp`, `.crx`, `.nex`, `.db`, `.sqlite`, `.sqlite3`, `.ldb`, `.pfx`, `.p12`, `.cer`, `.der`).

## [1.8.4] - 2026-10-01

### Added

- Ignore rules and binary extension filters for Rust core and Electron desktop applications (`.node`, `.pdb`, `.ilk`, `.rlib`, `.rmeta`, `.exp`, `.asar`, `.msi`, `.msix`, `.appx`, `.dmg`, `.pkg`, `.deb`, `.rpm`, `.appimage`, `.snap`, `.blockmap`).
- Excluded Electron desktop build directories (`dist_electron`, `release`, `releases`, `release-builds`, `.webpack`, `.vite`) and package manager debug logs (`npm-debug.log`, `yarn-debug.log`, `yarn-error.log`, `pnpm-debug.log`).

## [1.8.3] - 2026-08-26

### Changed

- Redesigned confirmation and prompt dialogs with compact adaptive sizing, clean bottom action buttons (Cancel / Save / Delete), and removed empty vertical whitespace.

## [1.8.2] - 2026-08-25

### Changed

- Highlighted token count badge in timeline history with distinctive border, contrast colors, and hover styling for quick metric visibility.

## [1.8.1] - 2026-08-13

### Changed

- Increased desktop typography, compact control labels, editor text, and action icon scale for clearer Windows readability.

## [1.8.0] - 2026-08-13

### Added

- Verified, architecture-aware updates with background state, startup handshake, rollback, and legacy API compatibility.
- Responsive desktop workspace with compact drawers, accessible dialogs, persistent UI preferences, and release notes.
- Windows amd64 and arm64 icon, DPI-aware manifest, long-path support, and executable version metadata.
- Release checksums and GitHub build-provenance attestations.

### Changed

- Refactored process ownership around a shared cancellation context and graceful HTTP shutdown.
- Added scoped nested `.gitignore` handling and bounded parallel project statistics.
- Streamed ordered document generation to atomic files with bounded memory.
- Replaced the unbounded token memoization map with a bounded collision-safe LRU.
- Split bookmark persistence into focused storage/history modules with atomic recovery.
- Added ranged content previews, download ranges, request limits, and a consolidated status endpoint.
- Replaced the 3-second UI heartbeat and full-document startup load with event-driven, cancellable requests.

### Fixed

- Exact release asset selection for the running OS and architecture.
- Binary integrity, executable format, and release ownership validation before applying an update.
- Shutdown races, duplicate saved paths, corrupt history handling, large-preview memory pressure, and titlebar icon ID mismatch.

[Unreleased]: https://github.com/vuducmynh/golang-count-your-codebase-token/compare/v1.8.5...HEAD
[1.8.5]: https://github.com/vuducmynh/golang-count-your-codebase-token/compare/v1.8.4...v1.8.5
[1.8.4]: https://github.com/vuducmynh/golang-count-your-codebase-token/compare/v1.8.3...v1.8.4
[1.8.3]: https://github.com/vuducmynh/golang-count-your-codebase-token/compare/v1.8.2...v1.8.3
[1.8.2]: https://github.com/vuducmynh/golang-count-your-codebase-token/compare/v1.8.1...v1.8.2
[1.8.1]: https://github.com/vuducmynh/golang-count-your-codebase-token/compare/v1.8.0...v1.8.1
[1.8.0]: https://github.com/vuducmynh/golang-count-your-codebase-token/compare/v1.7.8...v1.8.0
