# Beholden Coffee — Business-tier teaser guide

> **DDM paid-conversion revert process — perform only after owner sign-off.** This folder is currently a private teaser demo. To convert it into the paid client build: **(1)** delete the `<meta name="robots" content="noindex, nofollow">` line in `index.html`; **(2)** delete the teaser-demo submit-intercept block in `script.js` and set a real Formspree ID in the form action; **(3)** remove the `demo-banner` div from `index.html` and remove its offset JS from `script.js`. Then deploy to the client's own hosting and custom domain after owner sign-off.

This folder is a content-complete Beholden Coffee Business-tier teaser demo built from the DDM Business template. It is for presentation and review, not an official live site. Keep the noindex, intercepted-form, and concept-image boundaries intact until the owner approves the paid conversion.

**DDM Tier: Package B — Business (₱15,000–30,000 one-time).** The Business tier demonstrates a full on-site menu, photo gallery, reviews/testimonials, location details, and a stronger inquiry path. Confirm all client-specific content before launch.

## When to use this guide

- When presenting the Beholden Coffee Business-tier concept to a prospective owner.
- When converting this teaser into the paid build after deposit and owner sign-off.
- When cloning the DDM Business template for another approved DDM Business-tier site.

The current site-specific content is already complete in `index.html`; this guide records the reusable boundaries and handoff steps.

## What's in this Business-tier build

| Feature | Beholden Coffee teaser demo |
|---|---|
| One-page responsive layout | ✅ |
| Full on-site menu and pricing presentation | ✅, confirm before launch |
| Photo gallery section | ✅ |
| Reviews/testimonials section | ✅, confirm demo labeling and source |
| Location, hours, contact, and CTAs | ✅, confirm with owner |
| Inquiry form | Intercepted; no real submission |
| Search indexing | Disabled with `noindex, nofollow` |
| Concept imagery | Seven AI-generated images; no scraped/client photography |

## Content and asset boundary

The seven AI-generated concept images are `hero-pour-over-bar`, `bean-selection-ritual`, `coffee-flight`, `filipino-sharing-table`, `evening-cocktails`, `davao-creamy-mocha`, and `navy-amber-texture`. Their PNG/WebP pairs are alternate delivery formats. Do not describe them as client photography, real product photography, or photographs of a real branch. Do not add scraped photography.

Before paid launch, confirm all menu prices, review sources, hours, addresses, phone/email details, maps, and social links with the owner. Replace concept imagery only with approved assets.

## Clone and rebrand

This site was built from the DDM Business template. For a new approved Business-tier project, duplicate the approved template folder, rename the copy for the client, and replace the content, palette tokens, metadata, and approved assets while retaining the same teaser hardening until sign-off.

For this site, the existing palette in `styles.css` is the source of truth: amber `#E8A200`, deep navy `#13232D`, navy `#1D2F3A`, and cream `#FFF8E8`. Do not invent replacement colors in the manifest or deploy config.

## SEO and domain files

The neutral placeholder origin is `https://beholden-coffee-demo.netlify.app`. Keep it consistent in canonical metadata, Open Graph/Twitter URLs and images, JSON-LD, `robots.txt`, and `sitemap.xml` while this is a teaser. The sitemap `lastmod` is `2026-07-22`.

The teaser remains noindex. The paid-conversion process at the top of this file removes the noindex line only after owner sign-off and content confirmation.

## Deploy policy

This is a static site with no build step. Deploy the private teaser demo to Vercel first, alternating to Netlify based on Netlify's monthly credit availability. `vercel.json` and `netlify.toml` carry equivalent security and long-cache intent.

Vercel is a teaser-demo/portfolio target only while the account is on Hobby. Vercel Hobby must not host a paid commercial client build. Netlify is the sole production-commercial hosting target under DDM's current rule. After the three reversions and owner sign-off, deploy the paid site to the client's own hosting and custom domain.

## Handover checklist

- [ ] Owner approves the Beholden Coffee copy, menu, prices, hours, addresses, contact details, and social links.
- [ ] Demo reviews are replaced or explicitly approved as presentation placeholders.
- [ ] Any replacement photography is client-provided or otherwise licensed with permission.
- [ ] The noindex line is removed only for the approved paid build.
- [ ] The teaser submit intercept is removed and the real Formspree ID is set.
- [ ] The `demo-banner` div and its offset JS are removed.
- [ ] The paid build is deployed to the client's own hosting and custom domain.
- [ ] Canonical, JSON-LD, social metadata, robots, and sitemap are updated to the client's approved domain.
- [ ] `netlify.toml` remains the commercial production configuration unless DDM's hosting rule changes.
