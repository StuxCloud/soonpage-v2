# Contributing to soonpage-v2

Thank you for your interest in contributing! This repository is an archived, pinned snapshot of the green-era soonpage design, so its scope is intentionally narrow.

## Scope

This is **not** the actively developed template. That's [StuxCloud/soonpage](https://github.com/StuxCloud/soonpage). This repo preserves the pre-teal `v2` look as-is. Contributions here should keep the existing design working, not change it:

- Fixing broken links, encoding issues, or browser-compatibility bugs
- Keeping the page renderable as browsers and standards evolve

New features, redesigns, or styling changes belong in the live `soonpage` repository instead.

## Versioning and changelog

- The version lives in `VERSION.md` (a bare version string). Bump it on every release
- Every release gets a `CHANGELOG.md` entry using `### Added` / `### Changed` / `### Fixed` / `### Removed` / `### Security` / `### Deprecated` subsections, in that order
- `commit.sh` (bash) and `commit.bat` (Windows) read `VERSION.md` and handle the commit + `git tag` for a release
