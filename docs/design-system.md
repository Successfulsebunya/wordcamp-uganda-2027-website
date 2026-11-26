# Design system

The look is a dark editorial style built on the colours of the Uganda flag: black, yellow and red. Light "paper" sections give the eye a rest between dark bands.

All values below come from Global Styles ([`src/styles/global-styles.json`](../src/styles/global-styles.json)).

## Colour palette

| Slug | Name | Hex | Use |
| --- | --- | --- | --- |
| `accent` | Uganda Yellow | `#FCDD00` | Primary buttons, highlights on dark backgrounds |
| `uganda-red` | Uganda Red | `#DE0000` | Decorative accents, flag details |
| `uganda-red-text` | Uganda red (text) | `#B80000` | Red text on light backgrounds (passes contrast where `#DE0000` doesn't) |
| `ink` | Ink | `#0A0B0D` | Main text, dark sections |
| `paper` | Paper | `#F4F4F1` | Site background |
| `base` | Base (near-white) | `#F4F5F2` | Text on dark |
| `muted` | Muted (text on dark) | `#C9CBD0` | Secondary text on dark |
| `faint` | Faint (eyebrow on dark) | `#8A8C92` | Small labels on dark |
| `surface` | Surface (dark card) | `#14161C` | Cards on dark sections |
| `surface-2` | Surface 2 (raised dark) | `#0E0F12` | Raised dark cards |
| `line` | Line (dark hairline) | `#2A2B30` | Borders on dark |
| `muted-dark` | Muted Dark (text on light) | `#34343A` | Secondary text on light, link hover |
| `line-light` | Line Light (hairline) | `#DAD9D3` | Borders on light |
| `white` | White | `#FFFFFF` | Cards on light sections |

Rules of thumb:
- Yellow is for things on dark backgrounds. On white or paper, yellow text fails contrast, so use ink with a yellow shape behind it instead.
- Use `uganda-red-text` for red text, never `uganda-red`.

## Typography

| Role | Font | Where it's set |
| --- | --- | --- |
| Headings H1, H2 | **Anton** (custom font, weight 400) | Global Styles → Typography → Elements |
| Main menu | Anton | Additional CSS (navigation section) |
| Body text | **Manrope** (theme font, variable 200–800) | Theme default |
| Buttons | Manrope | Global Styles → Blocks → Button |
| Code | Fira Code (theme font) | Theme default |

Anton is a tall condensed display face. It's used in capitals for headings and short labels only, never for paragraphs.

## The pattern

The official WordCamp Uganda pattern runs as a thin band in three places:

- under the home page hero ("Pattern edge (hero)")
- under the page hero on every inner template ("Pattern edge (page hero)")
- at the top of the footer ("Pattern edge (footer)")

It's a Group block with class `wcu-pattern-edge`, a 24px minimum height and the pattern image as a repeating background, all set in block settings. The image is a lightweight PNG (411×48) rendered from the official SVG onto paper colour `#F4F4F1`. The same band appears at the bottom of the social share image.

The pattern artwork itself is not in this repository.

## Breakpoints

These are the widths the CSS responds to. Core block breakpoints (600px, 782px) are used where possible.

| Width | What changes |
| --- | --- |
| ≤ 360px | Smallest phones: ticket quantity stacks, compact cards |
| ≤ 599px / 600px | Phone layout, header search spans the header |
| ≤ 781px | Columns stack (WordPress core breakpoint) |
| 600–1199px | Menu button instead of the full menu |
| 782–1320px | Tighter header spacing so menu, search and ticket button fit |
| ≥ 1200px | Full menu |

The site is checked down to **240px** wide.

## Motion

Animations respect `prefers-reduced-motion`. Decorative motion (button shine, confetti, card hovers) is switched off for people who ask for less motion.

## Known exceptions

- **`!important`:** three declarations remain, all on news cards with a photo. WordPress preset text colour classes use `!important` themselves, so they can only be overridden the same way.
