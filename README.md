<p align="center">
  <img src="https://global.media.stux.cloud/v2/logo.png" height="100" alt="Stux.Cloud Logo">
</p>

# Coming Soon Page v2

*The green-era Stux.Cloud coming-soon page, preserved.*

An archived, pinned snapshot of [StuxCloud/soonpage](https://github.com/StuxCloud/soonpage), frozen at its `1f94d59` commit (`v1.1.2`): the last state of the page before Stux.Cloud moved from its two-tone green brand to the single teal `#07878e`. This repository exists so the green design stays available and independently versioned as `v2`, separate from the live template's ongoing development.

Live at [soonpage-v2.stux.cloud](https://soonpage-v2.stux.cloud/). Its logo, icon and favicon are pinned to the archived green assets under `https://global.media.stux.cloud/v2/`.

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/StuxCloud/soonpage-v2.git
   ```

2. Run it locally:

   ```bash
   ./dev-server.sh        # or dev-server.bat on Windows
   ```

   Then open the printed URL. You can also open `index.html` directly in your browser.

## Scope

This repository is an archive, not the actively developed template. Contributions are limited to fixes that keep this exact design working (broken links, encoding issues, browser compatibility). For new features or a redesign, see the live [soonpage](https://github.com/StuxCloud/soonpage) repository instead.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to get involved, and [CHANGELOG.md](CHANGELOG.md) for release history.

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

## Tests

Run `bash tests/version.sh` and `bash tests/site.sh` (Python 3.8+, no dependencies). The second checks the Discord link previews and the icon set. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Copyright (c) 2026 Stux.Group. This project is open source and available for use and modification.

---

*Stux.Cloud is part of the <img src="https://global.media.stux.group/icon.png" height="14" alt="Stux.Group" valign="middle"> Stux.Group Brand of Companies.*
