# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a documentation-only repository for a Pro Senectute Windows 11 basics workshop for seniors. All content is in German. Source files are written in AsciiDoc (`.adoc`) and stored in `docs/`. The CI/CD pipeline converts them to HTML and deploys to GitHub Pages.

## Build

The build is automated via GitHub Actions on push to `main`. To build locally:

```bash
mkdir -p build
find docs -name "*.adoc" -exec asciidoctor -D build {} \;
cp docs/*.pdf build
```

Requires `asciidoctor` to be installed (`sudo apt-get install -y asciidoctor` on Ubuntu, `brew install asciidoctor` on macOS).

## Repository Structure

- `docs/` — AsciiDoc source files (`.adoc`) and PDF handouts
- `.github/workflows/asciidoctor.yml` — Builds and deploys to GitHub Pages on push to `main`
- `build/` — Generated HTML output (not committed, produced by CI)

## Content Structure

Workshop spans 2 days (3 hours each, 09:00–12:00) and covers:

### Day 1

#### Focus on "Get to know Windows 11"

- Learn Windows 11
- Start menu customization
- WLAN connection setup
- Handling application windows

### Day 2

#### Focus on "Manage and save files"

- Storage options
    - Local Hard-Drive
    - USB-Stick
    - OneDrive
        - Explain One Drive
- File organization
    - Concepts of some naming strategies
- Document storage

## License

CC0 1.0 Universal — content is dedicated to the public domain.
