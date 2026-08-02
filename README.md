# NAPCheck

A free, single-page tool that helps small business owners keep their listings correct on Google, Apple Maps, Yelp, and Bing, generate robust schema markup for their website, and write a search title and description that won't get cut off in results.

Built by an SEO expert with 15+ years of hands-on experience helping local businesses get found. The checklist and schema fields are based on the same process used to audit real client listings.

## What it does

- **Business info form** — enter your name, address, phone, hours, business type, and a few optional details once.
- **Live schema markup** — generates ready-to-paste JSON-LD (`LocalBusiness` and 20+ specific subtypes like `Restaurant`, `SelfStorage`, `Plumber`, etc.), including structured opening hours, geo coordinates, service/offer catalogs, areas served, and links to your other listings (`sameAs`).
- **Where to add it** — step-by-step instructions for WordPress, Squarespace, Wix, Shopify, and custom HTML.
- **Search title & description generator** — auto-suggests both from your business info, with live character counters so you know exactly what will and won't get cut off in Google results.
- **Listing audit checklist** — a priority-ordered checklist (data aggregators first, then the primary listings, then industry-specific directories, then social) explaining *why* each one matters, not just a list of links.

## Why it's manual, not automatic

Google, Bing, and Apple don't offer a public API to look up someone else's business listing — Google's API only works once the actual owner signs in and grants access, and Yelp's terms don't allow storing or reusing their data outside their own widgets. So this tool doesn't scrape anything. You paste in what's currently live on a platform, or just work straight from the checklist. That's what keeps it free to run forever with no API costs and nothing to break when a platform changes its rules.

## Tech

Single self-contained `index.html` file. No build step, no backend, no dependencies to install. Fonts load from Google Fonts over CDN; everything else — the schema logic, the character counters, the checklist — runs entirely in the browser.

Form data and checklist progress are saved locally via `localStorage`, tied to whatever domain the file is served from.

## Running it

Just open `index.html` in a browser, or serve it from anywhere static — GitHub Pages, Netlify, your own hosting. No configuration needed.

### Deploying on GitHub Pages

1. Push `index.html` to this repo (rename it to `index.html` if it isn't already).
2. Go to **Settings → Pages**.
3. Set the source to the branch and folder containing `index.html`.
4. Save, wait a minute or two, then visit the URL GitHub provides.

## License

MIT — see [LICENSE](./LICENSE).
