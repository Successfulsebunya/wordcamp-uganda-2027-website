# Components

Each component is made of normal core blocks. A `wcu-` class in the block's **Advanced → Additional CSS class(es)** field connects it to its styles in [`custom.css`](../src/styles/custom.css). Size, colour and spacing stay in the block settings, so they can be edited without CSS.

To find a component's CSS, search `custom.css` for its class name or its section comment.

## Site-wide

| Component | Classes | What it does |
| --- | --- | --- |
| Header | `wcu-site-header`, `wcu-mainbar`, `wcu-brand`, `wcu-mainnav` | Sticky header with logo, menu, search and ticket button |
| Ticket button | `wcu-header-cta`, `wcu-ticket-cta` | Ticket-stub button with side notches and perforation. Shine on hover/focus only |
| Header search | `wcu-header-search` | Core Search block, button-only. When it opens, the menu steps aside and the bar takes its place, so it never pushes the ticket button. On phones the open bar spans the header |
| Mobile menu | core Navigation overlay | White overlay. The current page is marked with an ink dot (yellow fails contrast on white) |
| Pattern band | `wcu-pattern-edge` | Thin strip of the official pattern under heroes and above the footer |
| Page hero | `wcu-page-hero`, `wcu-crumbs` | Dark hero with breadcrumbs on inner pages. Uses the featured image when there is one |

## Home page

| Component | Classes | What it does |
| --- | --- | --- |
| Hero | `wcu-hero-cover`, `wcu-hero-copy`, `wcu-hero-ghost` | Photo cover, date pill "12–13 March 2027", venue line, ticket and secondary buttons |
| The two days | `wcu-days-grid`, `wcu-day-card`, `wcu-stamp`, `wcu-stamp-photo` | Two postage-stamp cards with perforated edges and a postmark (decorative) |
| Get involved | `wcu-way-mosaic`, `wcu-way`, `wcu-way-meta`, `wcu-way-link` | Photo mosaic. The whole card is the link |
| Uniquely Uganda | `wcu-uniq`, `wcu-uniq-grid`, `wcu-uniq-tile`, `wcu-uniq-photo`, `wcu-uniq-link` | Travel tiles (visa, invitation letter, arrival, health, weather). Two per row on tablet, one on small phones |
| Sponsor logos | `wcu-sponsor-logos` | Rows of three logos. Height is capped per logo so wide and tall marks look balanced. Greyscale, colour on hover |
| Latest news | `wcu-news`, `wcu-news-card`, `wcu-news-photo` | Query Loop of the newest posts. Cards with a photo are cut to the outline of Uganda |

## Content pages

| Component | Classes | What it does |
| --- | --- | --- |
| FAQ | `wcu-faq` | Core Details blocks styled as an accordion, with a jump list on the FAQ page |
| Travel guides | (section "Travel guides") | Numbered steps, key-value lists, sticky side card |
| Sponsorship packages | (section "Sponsorship packages v2", "Compare table") | Package cards with a ticket tear-line, add-on cards and a comparison table that scrolls sideways on phones |
| Sponsors page | `wcu-sponsor-grid` | WordCamp Sponsors block shown as an open logo wall that matches the home page |
| Organizers | `wcu-team-section`, `wcu-org-*` | Team grid with profile drawers made with `details`/`summary` (no JavaScript) |
| Single organizer | `wcu-pass`, `wcu-pass-stage` | Profile shown as an event pass |
| Blog cards | `wcu-post-grid`, `wcu-post-card`, `wcu-post-meta` | News archive cards |

## Decorative motifs

These carry the event's "travel" theme. All are decorative: they're hidden from screen readers or drawn in CSS, and motion is off with reduced motion.

- **Postage stamp:** perforated frame and postmark (The two days, letter cards)
- **Passport stamp:** tilted stamp (`wcu-btn-badge`)
- **Boarding pass:** notched stub with perforation
- **Ticket notch:** side notches on cards that carry the pattern

## Icons

Icons are [Lucide](https://lucide.dev/) SVGs (ISC licence), stored as CSS custom properties (`--wcu-icon-*`) and drawn with CSS `mask`, so they take the text colour.
