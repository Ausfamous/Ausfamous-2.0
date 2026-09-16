# Ausfamous: deploy to Vercel

A static site with no build step.

1. Go to vercel.com/new and choose "Deploy" with this folder, or run `npx vercel --prod` from this folder.
2. Framework preset: **Other**. Leave the build command empty. The output directory is `.` (this folder).
3. Add the domain ausfamous.com under Project → Domains.

## What's inside

- `index.html` plus prerendered pages for each story, section, city guide and the two Ausfamous 100 lists. Every page has full metadata.
- `agency.html` is served at `/agency`. It keeps the current agency page and adds: a scroll-driven hero (your Creation artwork, then Melbourne → every Australian capital → the world), featured Grant, Olivia and James in In Good Company, a Before & After sector journey, and scroll-animated process and outcomes. Pricing is removed for now, and visitors who prefer reduced motion get a static version. The old `/agency/apply`, `/agency/process` and `/agency/mandates` URLs redirect to the matching section.
- `vercel.json` sets clean URLs, redirects and cache headers. The folder also includes `manifest.webmanifest`, `sw.js`, `robots.txt`, `sitemap.xml`, `404.html` and the icons.
- `img/credits.json` lists the Unsplash photographers.

## Before launch

- Add the real LinkedIn, Facebook and YouTube URLs. They currently point to "#".
- The enquiry form shows a thank-you message and opens an email to become@ausfamous.com.au. To store submissions, connect a form service such as Formspree.
