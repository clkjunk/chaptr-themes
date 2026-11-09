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