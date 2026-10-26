# Changelog

All notable changes to soonpage-v2 are documented here.

Since v26.10.23 this project uses [Date Versioning](https://datevers.ing) (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used Semantic Versioning.

## v26.10.26

### Security

- CI uses Node.js 24 instead of the end-of-life Node.js 20, which has no fix for the Brotli decoder vulnerability CVE-2026-111497

## v26.10.23-1

### Added

- A full icon set from the brand's own icon: `favicon.ico` (16, 32 and 48px) and `apple-touch-icon.png` at the site root, and a `site.webmanifest` with 192px, 512px and maskable icons, so the page has a proper icon in browser tabs, bookmarks and on phone home screens (the home-screen icons sit on a white background, as iOS would otherwise fill the icon's transparent corners with black). Every page lists the same icons, served from this site instead of the media host
- Discord link previews: sharing any page in Discord shows a custom preview in the Stux.Cloud brand colour, with the page's name, what it is and a few links (Stux.Cloud on the coming-soon page; the legal pages link back to Boring Legal Stuff). Names and descriptions show as plain text, and the 404 page has none. They're pre-built into each page by `python scripts/build-discord-embeds.py`, which `scripts/build-sitemap.py` now runs too
- `tests/site.sh`, which checks that every preview is valid JSON under Discord's 3,000-byte limit and none is on the 404 page, that the icon files have the right sizes, and that every page's `<head>` carries the same icon tags. CI runs it

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v2.0.4
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## v2.0.4

### Fixed

- The footer's copyright line had a second, hidden copy of the © icon inside its screen-reader text; it's gone, leaving the visible icon and a plain "©" for screen readers. Nothing changes on screen

## v2.0.3

### Changed

- The footer no longer says "Stux.Cloud is operated by Stux Group Ltd."; that belongs on the Imprint, which still says it. The copyright line names Stux.Cloud instead of Stux.Group ("© 2026 Stux.Cloud. All rights reserved.")

## v2.0.2

### Fixed

- The light/dark choice was saved in the browser under `stuxedo-theme`, a name left over from the Stuxedo page this design was built from; it's now `stuxcloud-theme` on every page, and the Cookies Policy names it correctly. Nothing else in this archived design changes

## v2.0.1

### Fixed

- The imprint said this page is published as Stux.Cloud, "which is operated by Stux.Cloud, which is operated by" Stux Group Ltd, repeating itself; it now reads "published as Stux.Cloud, which is operated by" Stux Group Ltd

## v2.0.0

### Added

- Archived [StuxCloud/soonpage](https://github.com/StuxCloud/soonpage) at commit `1f94d59` (`v1.1.2`), the last state before Stux.Cloud's rebrand from two-tone green to single teal, preserving history up to that point as this repository's own `main` branch

### Changed

- Served from `soonpage-v2.stux.cloud` instead of `soonpage.stux.cloud` (CNAME, canonical URLs, sitemap and robots.txt)
- Logo, icon and favicon now point at the archived green assets under `https://global.media.stux.cloud/v2/` instead of the live Stux.Cloud brand assets, which are now teal
- README and CONTRIBUTING describe this repository as an archive
