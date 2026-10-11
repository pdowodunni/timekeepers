# TimeKeepers – new home page (design preview)

Two design directions for the new timekeepers-ng.com home page. Each is a single, self-contained HTML file.

| Folder | Version |
| --- | --- |
| `dark/` | Fully dark |
| `half-and-half/` | Dark and light sections alternating, full-width photography |
| `/` (root) | Start page linking to both versions |

## Netlify

**Two separate sites (one per version):** in Netlify, *Add new site → Import an existing project → GitHub → this repo*, then set:

| Site | Base directory | Build command | Publish directory |
| --- | --- | --- | --- |
| Dark | *(empty)* | *(empty)* | `dark` |
| Half & half | *(empty)* | *(empty)* | `half-and-half` |

**Or one site with everything:** leave base directory empty and publish directory `.`, giving `/`, `/dark/` and `/half-and-half/`.

There is no build step. Every push to `main` redeploys automatically. The `_headers` files keep the previews out of search engines (`noindex`).

## For developers

Read the notes at the top of each `index.html` first. Important: put the page on the demo server first, never straight to live; add the SEO, analytics and sharing tags listed in the `<head>`; and confirm image usage (the KYROS photos in Half & half are KYROS brand photography) with Daniel.
