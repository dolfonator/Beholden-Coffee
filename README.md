# Beholden Coffee — Business-tier teaser demo

Beholden Coffee is a content-complete, one-page Business-tier teaser demo for a specialty coffee, Filipino kitchen, and cocktail bar concept in Davao City. It is built from the DDM Business template with plain HTML, CSS, and JavaScript: no framework, no dependencies, and no build step.

This is a private presentation artifact, not an official Beholden Coffee website. The site is noindex, the inquiry form is intercepted by `script.js`, and nothing is submitted to a real backend. The neutral placeholder origin for site metadata is `https://beholden-coffee-demo.netlify.app`.

## What's inside

```
Beholden Coffee/
├── index.html          ← content-complete one-page teaser demo
├── thanks.html         ← noindex concept-confirmation page
├── styles.css          ← navy/amber design system and responsive layout
├── script.js           ← navigation, reveal effects, and demo form intercept
├── vercel.json         ← Vercel security and asset-cache headers
├── netlify.toml        ← Netlify static publish, headers, cache, and redirect
├── site.webmanifest    ← Beholden Coffee install metadata and existing icons
├── robots.txt          ← crawl rules and placeholder sitemap URL
├── sitemap.xml         ← placeholder-origin sitemap
├── favicon.ico         ← site favicon
├── TEMPLATE-GUIDE.md   ← clone, handoff, and paid-conversion instructions
├── PRODUCT.md          ← product intent, boundaries, and hosting policy
└── assets/             ← seven AI-generated concept-image families plus icons
```

## Asset boundary

The site uses seven AI-generated concept images: `hero-pour-over-bar`, `bean-selection-ritual`, `coffee-flight`, `filipino-sharing-table`, `evening-cocktails`, `davao-creamy-mocha`, and `navy-amber-texture`. PNG and WebP files are delivery formats for those concepts; they do not represent fourteen separate image concepts. No scraped or client photography is included.

## Deploy targets

This static folder has no build command. DDM's standing workflow is to deploy the private teaser demo to Vercel first, then use Netlify when Netlify's monthly credit availability calls for it. The generated platform URL is only a preview/portfolio destination; the canonical, social, JSON-LD, sitemap, and robots references remain on the neutral placeholder origin above.

`vercel.json` mirrors the security and long-cache intent of `netlify.toml`. Vercel is permitted here for the private noindex teaser demo and portfolio presentation. Under DDM's standing hard rule, Vercel Hobby is not for commercial client use. Paid/converted client builds use Netlify as the production-commercial host for this project.

For the paid handoff, deploy to the client's own hosting and custom domain only after owner sign-off. The three required code reversions are documented at the top of `TEMPLATE-GUIDE.md`.

## Local preview

```bash
python3 -m http.server 8080
# open http://127.0.0.1:8080
```

Use a local server instead of double-clicking `index.html`, so root-absolute paths such as `/styles.css` and `/assets/...` resolve correctly.

## Before paid conversion

- Confirm Beholden Coffee's menu, prices, hours, addresses, phone, email, and social links with the owner.
- Treat all menu prices and demo reviews as presentation content until the owner approves the final copy.
- Obtain permission for any future client photography; replace concept imagery only with approved assets.
- Keep the noindex and intercepted-form hardening active until owner sign-off.

*Built for the DDM local-business website project. Tech: plain HTML/CSS/JS · Teaser deploy: Vercel first, Netlify alternate · Commercial production: Netlify only under the current account rule · Currency: PHP.*
