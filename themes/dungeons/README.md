# Dungeons

A high-fantasy theme for tabletop roleplaying documents. It styles stat blocks
written with Chaptr's generic classed-container syntax; Chaptr itself does not
define game-specific monster markup.

This theme requires Chaptr 0.1.2 or newer.

## Stat Blocks

Use the `monster-card` CSS class and exclude the creature's headings from the
document table of contents:

```markdown
::: monster-card toc=exclude
## Example Creature
*Medium humanoid*

**AC:** 12

**HP:** 40

| STR | DEX | CON |
| --- | --- | --- |
| 9 (-1) | 14 (+2) | 11 (+0) |

### Actions
**Strike.** Write the complete action here.
:::
```

Include only the sections needed. Leave a blank line between paragraphs; two
trailing spaces create a line break within a paragraph. The closing delimiter
must be in the same chapter.

In `document.yaml`, select `theme: dungeons`. Keep personal CSS in the project's
separate `stylesheet` file. Updating the downloaded theme replaces this theme's
files, but does not replace the project stylesheet.

## Layout

Chaptr's base stylesheet supplies columns, alignment, responsive images and
tables. Dungeons adds the fantasy-specific presentation. Use `columns` for
two equal columns, `columns columns-3` for three, `columns columns-2-1` for
a wide left column or `columns columns-1-2` for a wide right column.

For example, place encounter text beside a stat block. Use a longer delimiter
for each nesting level: five colons for the layout, four for each column and
three for the stat block.

```markdown
::::: columns columns-2-1
:::: column
## Encounter

Describe the location and encounter here.
::::

:::: column
::: monster-card toc=exclude
## Example Creature
*Medium humanoid*

**AC:** 12

**HP:** 40

### Actions
**Strike.** Write the complete action here.
:::
::::
:::::
```

Columns are independent blocks and do not automatically flow text between
them. Narrow screens stack them in reading order; print preserves their
widths. Use `align-left`, `align-center`, `align-right` or `align-justify`
on a container for text alignment. Left, center and right also position images.
Keep layout overrides in the project stylesheet and check the rendered PDF,
especially when stat blocks or columns are long.