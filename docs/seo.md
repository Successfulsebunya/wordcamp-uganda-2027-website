# SEO and social sharing

SEO uses **Jetpack**, which is active on WordCamp.org. There's no other SEO plugin.

## Per page and post

Each page and post has, in the editor sidebar under Jetpack SEO:

| Field | Meta key | Guideline |
| --- | --- | --- |
| SEO title | `jetpack_seo_html_title` | Under 60 characters. Lead with the page topic, end with "WordCamp Uganda 2027" where it fits |
| Meta description | `advanced_seo_description` | 140–160 characters. Say what the page answers, include "Kampala" or "2027" where natural |
| Hide from search | `jetpack_seo_noindex` | Only for utility pages |

The same description is used for social previews (Open Graph and X cards) when the page has no custom excerpt.

## Home page

- **Title:** includes the dates and venue, so the preview shows them even before anyone clicks.
- **Front page description:** set in Jetpack settings (`advanced_seo_front_page_description`).
- **Share image:** `wordcamp-uganda-2027-share.jpg`, 2400×1260 (1.91:1), a photo with the event name, dates, venue and the pattern band at the bottom. It's the home page's featured image, which Jetpack uses for `og:image`.

## Keywords

WordCamp Uganda 2027, WordPress conference Uganda, WordPress Kampala, WordCamp Kampala, tech conference Uganda 2027, Contributor Day.

They're used in titles, headings and descriptions where they read naturally, never stuffed.

## Images

- Photos are compressed and sized for their slot before upload.
- Give every content image alt text. Leave alt empty on decorative images.
- Unused media is deleted, so the media library stays small.

## Refreshing a stale preview

Social apps cache previews. After changing a title, description or share image:

- **Facebook / WhatsApp:** open the [Sharing Debugger](https://developers.facebook.com/tools/debug/), paste the URL and click **Scrape Again**. WhatsApp uses the same cache.
- **LinkedIn:** use the [Post Inspector](https://www.linkedin.com/post-inspector/).
- **Quick test:** share the URL with `?v=2` at the end. A new URL gets a fresh preview.
