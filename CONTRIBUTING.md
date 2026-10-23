# Contributing to soonpage-v2

Thank you for your interest in contributing! This repository is an archived, pinned snapshot of the green-era soonpage design, so its scope is intentionally narrow.

## Scope

This is **not** the actively developed template. That's [StuxCloud/soonpage](https://github.com/StuxCloud/soonpage). This repo preserves the pre-teal `v2` look as-is. Contributions here should keep the existing design working, not change it:

- Fixing broken links, encoding issues, or browser-compatibility bugs
- Keeping the page renderable as browsers and standards evolve

New features, redesigns, or styling changes belong in the live `soonpage` repository instead.

## Discord previews and icons

- Every page except `404.html` has a Discord link preview: a pre-built `<script id="discord:component-embed">` block in its `<head>`, written by `python scripts/build-discord-embeds.py` from the page's `<title>` and `<meta name="description">` (the coming-soon page's text and buttons are set at the top of the script; `build-sitemap.py` runs it too). Re-run it after changing a page's title or description or adding a page; `--check` only reports stale pages
- The icon set is `favicon.ico`, `apple-touch-icon.png`, `site.webmanifest` and `assets/img/icon-*.png`. Every page's `<head>` carries the same four tags for them (`favicon.ico`, `icon-512.png`, `apple-touch-icon.png`, `site.webmanifest`); copy them as-is into any new page
- `bash tests/site.sh` (Python 3.8+, no dependencies) checks every preview and the icon set; CI runs it with `tests/version.sh`

## Versioning

This project uses [Date Versioning](https://datevers.ing). To release:

1. Add a `## vYY.MM.DD` entry at the top of `CHANGELOG.md`, with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set `VERSION.md` to the same bare version (no `v`): today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Use UTC, not local time: just after midnight in the UK it is still the previous day in UTC.
3. Run `bash tests/version.sh` and `bash tests/site.sh`.
4. Run `./commit.sh` (or `commit.bat` on Windows). It checks the version, commits and tags `vYY.MM.DD`, and never pushes.
