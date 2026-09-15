# Ausfamous — website (Vercel-ready)

Static, prerendered site. No build step required.

## Deploy
**Option A — Vercel dashboard:** New Project → drag-and-drop this folder (or import a Git repo containing it). Framework preset: **Other**. Build command: *none*. Output directory: `.` (root).

**Option B — CLI:**
```bash
npm i -g vercel
cd ausfamous-site
vercel          # preview
vercel --prod   # production
```
Then add the domain `ausfamous.com` (and `www.ausfamous.com` → redirect) in Project → Settings → Domains.

## What's inside
- `index.html` + prerendered pages for every route (`/story/…`, `/section/…`, `/register/all-time`, `/register/living`, `/guides`, `/guide/…`, `/agency`, `/agency/apply` …) for fast first paint and SEO. `cleanUrls` serves them without `.html`.
- `assets/app.css`, `assets/app.js` — the whole app (client-side routing after first load).
- `img/` Unsplash photography (credits in `img/credits.json`), `brand/` logo cut-outs, `icons/` favicons & app icons, `og-image.jpg` social card.
- `site.webmanifest` (installable app), `sw.js` (offline cache), `robots.txt`, `sitemap.xml`, `404.html`, `vercel.json` (clean URLs, caching, security headers).

## To finish before launch
1. **Social links:** LinkedIn, Facebook and YouTube URLs weren't on the live site. Add them in `assets/app.js` → `const SOCIAL` (empty entries are hidden) and in the JSON-LD `sameAs` in each HTML head.
2. **Logo:** the logo files were cut from a 611px image. Supply an SVG or 3000px PNG for sharper retina rendering and replace the files in `brand/`.
3. **Enquiry form:** it prepares an email / WhatsApp message (no server). To collect submissions directly, connect Formspree, Vercel Forms/Functions or your CRM.
4. **Content:** stories are researched to 16 September 2026 with sources on each page; review the Registers and City Guides before publishing.
5. After editing `assets/app.js`, the prerendered HTML still hydrates from the new JS, but re-run the build (source project) to refresh the static snapshots for SEO.
