# SEO audit: why the site may not rank for "mobile sports massage Sheffield"

## Key blockers found in codebase

1. **No dedicated indexable page for the target service query**
   - The strongest content for "mobile sports massage" exists in `_locations/mobile-sports-massage-we-come-to-you.md`.
   - However, in `_config.yml`, the `locations` collection has `output: false`, so Jekyll does **not** generate a standalone URL for that page.
   - This means Google only sees that text embedded in `/locations`, rather than a dedicated, highly relevant landing page.

2. **Generic `<title>` across pages**
   - `_layouts/default.html` hard-codes `<title>The Bodywork Hut</title>` for every page.
   - There is no page-level title support (e.g., including "Mobile Sports Massage Sheffield").

3. **Weak/duplicated meta descriptions**
   - `_layouts/default.html` outputs a generic description (`The Bodywork Hut`) and then conditionally outputs another meta description.
   - Multiple/duplicated description tags can dilute clarity for search engines.

4. **Template social meta still points to third-party demo URLs**
   - Open Graph and Twitter URLs/images point to `uideck.com` template assets instead of this domain.
   - This signals an incompletely customized template and weakens topical/site identity.

5. **No evidence of technical SEO basics in repo**
   - No `robots.txt` found.
   - No generated `sitemap.xml` setup found.
   - No canonical tag implementation found in the layout.

## Why this hurts this specific keyword

The query "mobile sports massage Sheffield" is local + service-intent. Google typically favors pages with:
- exact/close-match intent in title + headings,
- a dedicated URL focused on that service/location,
- strong local trust signals.

Right now, the strongest matching phrase appears in body content, but key ranking signals (title tag, indexable dedicated URL, canonical/technical hygiene) are under-optimized.

## Fastest fixes to prioritize

1. Set `collections.locations.output: true` and create a dedicated page URL for mobile service.
2. Make `<title>` dynamic from front matter, and optimize page title for target intent.
3. Keep exactly one meta description per page.
4. Replace all `uideck.com` OG/Twitter values with real site URLs/assets.
5. Add `robots.txt`, sitemap generation, and canonical tags.
