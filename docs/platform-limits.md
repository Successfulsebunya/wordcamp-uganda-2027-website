# Platform and limits

WordCamp sites run on the shared WordCamp.org network. Organisers get a site, not a server. Knowing the limits up front saves a lot of time.

## What I can't do

| Limit | What it means in practice |
| --- | --- |
| No plugin installs | Only platform-provided plugins: CampTix, Jetpack, WordCamp blocks and a few others |
| No custom JavaScript | Interactive things (menus, drawers, search) use core blocks or CSS-only techniques such as `details`/`summary` and `:target` |
| No theme files | No `functions.php`, no `theme.json` edits, no child theme. Twenty Twenty-Five is customised in the Site Editor only |
| No custom fonts upload through the theme | Anton is registered as a custom font in Global Styles and served from the site's media files |
| Jetpack Search is not active | It needs a paid plan, so site search uses the core Search block and the `search` template (no live results) |

## What I use instead

- **Global Styles** for palette, fonts and element styles, so anyone can change them in the Site Editor without touching CSS.
- **Block settings** for size, colour and spacing on each block.
- **Additional CSS** (Global Styles → Additional CSS) only for what block settings can't do: layout tricks, decorative shapes, responsive fixes and plugin output such as the CampTix form.
- **Synced patterns** for sections used on more than one page.
- **Template parts** for the header and footer.

## Working rules I follow

1. If a block setting can do it, use the block setting, not CSS.
2. Fonts are set only in Global Styles.
3. CSS stays scoped to `wcu-` class names added in the block's **Additional CSS class(es)** field, with low specificity so block panel edits still win.
4. Avoid `!important`. The few that remain are documented in [design-system.md](design-system.md#known-exceptions).
5. After every change to Global Styles, check that the rest of the styles are unchanged (see [maintaining.md](maintaining.md)).
