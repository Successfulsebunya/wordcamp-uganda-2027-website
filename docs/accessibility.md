# Accessibility

The target is **WCAG 2.2 AA**.

## What's in place

- **Contrast:** colours are chosen in pairs that pass AA. Yellow is only used on dark, red text uses `uganda-red-text` (`#B80000`). The mobile menu marks the current page in ink because yellow on white fails.
- **Focus:** every link, button and form control has a visible focus outline, including the CampTix form and the header search.
- **Keyboard:** menus, the search toggle, FAQ items and organiser drawers all work with the keyboard. Drawers use `details`/`summary`, which browsers make keyboard-accessible.
- **Touch targets:** ticket form controls are 48px tall.
- **Reduced motion:** all decorative animation is off under `prefers-reduced-motion: reduce`.
- **Decorative art:** stamps, confetti, the pattern artwork band and icons are decorative and hidden from assistive tech.

## Small screens

The site is checked down to **240px** wide. At 240px the logo, menu button, search and ticket button still fit in the header, and the ticket table doesn't overflow.

## How to check a change

1. Use one H1 per page and keep headings in order.
2. Give every content image alt text. Leave alt empty on decorative images.
3. Tab through the page from the top. Every interactive element should show focus and be reachable.
4. Zoom to 200%. Nothing should overlap or be cut off.
5. Check new colour pairs with a contrast checker.
6. Turn on reduced motion in your operating system and reload.
7. Resize to 240px.
