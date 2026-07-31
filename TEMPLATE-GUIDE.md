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
| Logo and concept imagery | Original generated logo plus seven AI-generated image families; no scraped photography |

## Content and asset boundary

The site includes an original abstract `beholden-mark` generated from an authorized client-owned reference, plus seven AI-generated concept-image families. The active page uses `hero-pour-over-bar`, `bean-selection-ritual`, `coffee-flight`, `davao-creamy-mocha`, and `navy-amber-texture`; `filipino-sharing-table` and `evening-cocktails` are retained but unused. PNG/WebP pairs are alternate delivery formats. Do not describe concept imagery as real product photography or photographs of a real branch, and do not add scraped photography.

Before paid launch, confirm the logo, official social-menu transcription, rotating menu availability, reviews, hours, C.M. Recto address, phone/email details, map, and social links with the owner. Replace concept imagery only with approved assets and obtain independent trademark advice if needed.

## Clone and rebrand

This site was built from the DDM Business template. For a new approved Business-tier project, duplicate the approved template folder, rename the copy for the client, and replace the content, palette tokens, metadata, and approved assets while retaining the same teaser hardening until sign-off.

For this site, the existing palette in `styles.css` is the source of truth: amber `#E8A200`, deep navy `#13232D`, navy `#1D2F3A`, and cream `#FFF8E8`. Do not invent replacement colors in the manifest or deploy config.

## SEO and domain files

The placeholder origin is `https://demo-beholdencoffee.netlify.app` — 13 references across `index.html`, `thanks.html`, `robots.txt`, `sitemap.xml`, and `site.webmanifest`. Keep it consistent in canonical metadata, Open Graph/Twitter URLs and images, JSON-LD, `robots.txt`, and `sitemap.xml` while this is a teaser. The sitemap `lastmod` is `2026-07-22`.

> Verify the origin against the URL actually presented before sending any link. A metas-vs-live mismatch renders a broken link preview in Messenger/Viber — it has already happened twice on other DDM teasers.

The teaser remains noindex. The paid-conversion process at the top of this file removes the noindex line only after owner sign-off and content confirmation.

## Deploy policy

This is a static site with no build step. Deploy the private teaser demo to Vercel first, alternating to Netlify based on Netlify's monthly credit availability. `vercel.json` and `netlify.toml` carry equivalent security and long-cache intent.

Vercel is a teaser-demo/portfolio target only while the account is on Hobby. Vercel Hobby must not host a paid commercial client build. Netlify is the sole production-commercial hosting target under DDM's current rule. After the three reversions and owner sign-off, deploy the paid site to the client's own hosting and custom domain.

## Activating the inquiry form (paid conversion)

**No backend is ever added.** The form posts to **Formspree**, a third-party endpoint, so the site stays plain static HTML with no build step and no server. Revert step (2) at the top of this file is the summary; this is the full procedure.

### What currently keeps the form inert

| Piece | State today | Where |
|---|---|---|
| Form `action` | placeholder `https://formspree.io/f/YOUR_FORM_ID` | `index.html:457` |
| Submit intercept | `preventDefault()` → `/thanks.html`, no network call | `script.js:73-80` |
| `_subject` / `_next` hidden fields | point at `demo-beholdencoffee.netlify.app` | `index.html:458-459` |

A prospect can fill the form in during a demo and get a convincing thank-you page, with nothing sent anywhere.

### Steps, in order

1. **Create the form** at <https://formspree.io> → Dashboard → New form → copy the ID after `/f/`. Create it under **the client's own account** where possible — same principle as registering the domain under the client and managing it on their behalf.
2. **Replace `YOUR_FORM_ID`** in the form `action` at `index.html:457`.
3. **Delete the teaser-demo intercept block** in `script.js` (lines 73–80, the whole commented block). Leaving it in place silently swallows every real submission — the form will look like it works and send nothing.
4. **Update the two hidden fields** at `index.html:458-459` to the client's final domain:
   - `_subject` — the subject line the client sees on every notification email.
   - `_next` — the post-submit redirect. **If this still points at the demo Netlify URL, a real customer is bounced to a dead host after submitting.** This is the step most often missed.
5. **Update `thanks.html`** — its canonical (`thanks.html:9`) also carries the demo origin.
6. **Confirm the address.** Formspree requires the destination address to be confirmed on the first submission; until someone does that, the form is silently inert. Send one real test submission and verify it (a) lands in the client's inbox and (b) redirects to `thanks.html`.

### Do not remove

- **The honeypot.** `_gotcha` at `index.html:460` is spam protection Formspree reads natively. It is not a demo artifact — keep it.
- **The `required` attributes and `autocomplete` hints** on the fields; they are the accessibility/UX baseline, not scaffolding.

### Scope note for the client conversation

The free Formspree tier caps monthly submissions. That is ample for a café inquiry form, but if volume ever exceeds it the fix is a paid upgrade **on the client's own Formspree account**, not a rebuild. Raise it at scoping so it never reads as a surprise later.

## Handover checklist

- [ ] Owner approves the Beholden Coffee logo, copy, menu, prices, rotating items, hours, C.M. Recto address, contact details, and social links.
- [ ] Demo reviews are replaced or explicitly approved as presentation placeholders.
- [ ] Any replacement photography is client-provided or otherwise licensed with permission.
- [ ] The noindex line is removed only for the approved paid build.
- [ ] The teaser submit intercept is removed and the real Formspree ID is set.
- [ ] `_subject` and `_next` are updated to the client's final domain (not the demo Netlify URL).
- [ ] The Formspree destination address is confirmed, and one real test submission has landed in the inbox and redirected to `thanks.html`.
- [ ] The `demo-banner` div and its offset JS are removed.
- [ ] The paid build is deployed to the client's own hosting and custom domain.
- [ ] Canonical, JSON-LD, social metadata, robots, and sitemap are updated to the client's approved domain.
- [ ] `netlify.toml` remains the commercial production configuration unless DDM's hosting rule changes.
