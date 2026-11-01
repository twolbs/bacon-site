# Bacon Basics and Beyond

A responsive food-magazine website built with semantic HTML, CSS and a little vanilla JavaScript. No backend, paid service, package manager or build process is required.

## Publish using GitHub Pages

1. Commit these files to the `main` branch of `twolbs/bacon-site`. If reviewing a pull request, merge it first.
2. Open the repository on GitHub and choose **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose **main** and **/ (root)**, then click **Save**.
5. Wait for the Pages deployment to finish. The site will be at **https://twolbs.github.io/bacon-site/**. GitHub shows the final URL and deployment status in Settings → Pages.

All asset links are relative, so the site works under the `/bacon-site/` project path. Do not select `archive/` as the publishing folder. If Pages is already configured to use GitHub Actions, switch to branch deployment or retain your existing static publishing workflow.

## Preview locally

Open `index.html` directly in your browser, or run `python3 -m http.server 8000` from this directory and visit http://localhost:8000. A local server is optional.

## Files

- `index.html` — homepage, educational sections, three full recipes and shopping links.
- `assets/styles.css` — warm editorial design, responsive layouts, keyboard focus and print styles.
- `assets/script.js` — accessible mobile navigation and recipe deep links.
- `assets/images/` — original SVG illustration placeholders, stored locally.
- `archive/original-index.html` — preserved original starter page.
- `.nojekyll` — tells GitHub Pages to serve the static files directly.

## Add your photographs

Replace the SVG illustrations with photos you own or have permission to publish. Update each image's `src`, descriptive `alt`, `width` and `height` in `index.html`. The hero uses `hero.svg`; recipe cards use `maple.svg`, `blt.svg` and `pasta.svg`; the author image uses `portrait.svg`. Remove the placeholder wording from alternative text when real photos are added. Keep images compressed, ideally WebP or JPEG. CSS crops images to consistent card sizes.

The SVGs are intentionally labeled illustrated photo placeholders. No stock photography or external image service is required. Typography optionally loads free Google Fonts; Georgia and Arial are local fallbacks if the visitor is offline or blocks font requests. To avoid external font requests entirely, remove the first `@import` line of `assets/styles.css`.

## Editing content

Recipes are native HTML `details` elements: they work without JavaScript. Links such as `#recipe-maple` also open the corresponding recipe when JavaScript is enabled. The mobile menu falls back to visible links without JavaScript. All six topic sections have stable navigation anchors.

Charlie and the About Me biography are explicitly fictional. Replace them with your own biography when ready. Retailer links are browsing resources, with no affiliate tracking, checkout, endorsements or claim of live prices. Review external links periodically.

Historical and regional summaries are introductory; naming varies by country and producer. Food safety guidance links to the USDA. Recipe timing depends on bacon thickness and equipment; follow package cooking instructions. This project does not offer home-curing instructions.
