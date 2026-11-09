# Theme Directory Guide

Each theme lives in its own directory, named with a lowercase ID containing
letters, digits or hyphens:

```text
themes/
  dungeons/
    dungeons.css
    README.md
    LICENSE
    preview.png
```

`preview.png` is optional. The CSS filename must match the directory ID so
Chaptr can install it as `themes/<theme-id>/<theme-id>.css` in a document
project.

Put a theme's purpose, visual details and usage notes in its README. Include
the applicable license for the theme and any assets it contains. The theme's
version, compatibility, release archive URL and checksum belong in the root
`catalog.json` entry.