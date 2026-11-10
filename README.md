# Chaptr Themes

Optional CSS themes for Chaptr document projects. Chaptr supplies a neutral
`base` stylesheet for typography, headings, tables, images, columns, alignment
and print layout. This repository provides distinct visual styles and
theme-specific components on top of that foundation.

Simple font, size or spacing changes can live in a project's `styles.css`
with `stylesheet: styles.css`; they do not require a separate theme.

## Catalog

`catalog.json` is the machine-readable index used by Chaptr to list available
themes. Each entry describes a theme and identifies its latest release archive.
Keep the version, archive URL and SHA-256 checksum in sync whenever a theme is
released or updated. Add a catalog entry when its versioned release archive is
published; source files alone are not installable from the catalog.

## Theme Files

Add one directory per theme under `themes/`. See [the theme directory guide](themes/README.md)
for the expected files and naming rules.

## Publishing or Updating a Theme

1. Make the theme CSS, README and license available under `themes/<theme-id>/`.
2. Package those files in a versioned ZIP archive and publish it as a GitHub Release.
3. Add or update the theme's catalog entry with its version, description, license,
   minimum Chaptr version, release archive URL and SHA-256 checksum.
4. Review the catalog and archive together before merging the change.

Use a new theme version for every published change. Do not replace an existing
release archive; older projects should continue to be able to download the
version they installed.

Updating a theme in a document project replaces the downloaded theme files.
Users should keep their own CSS overrides in the project's `stylesheet` file
rather than editing the downloaded theme files.

## Catalog Entry

Each object in the `themes` array uses this shape:

```json
{
  "id": "dungeons",
  "name": "Dungeons",
  "description": "A theme for fantasy roleplaying documents.",
  "version": "1.0.0",
  "license": "MIT",
  "min_chaptr_version": "0.1.2",
  "archive_url": "https://github.com/clkjunk/chaptr-themes/releases/download/dungeons-1.0.0/dungeons-1.0.0.zip",
  "sha256": "replace-with-the-archive-sha256"
}
```

The example is illustrative only; it is not an available theme.