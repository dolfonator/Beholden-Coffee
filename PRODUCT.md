# Product — Beholden Coffee

## Register

brand: Beholden Coffee
tier: Business
status: private teaser demo
template: DDM Business template

## Users

The primary audience is a restaurant owner or prospect reviewing the Beholden Coffee concept and deciding whether to commission the Business-tier build. This page is a sales and sign-off artifact, not a live ordering or reservation experience for diners.

## Product purpose

The Beholden Coffee Business-tier teaser demonstrates the step up from a simpler one-page restaurant package: a full on-site menu, a photo gallery, a reviews section, richer location and contact content, and a more complete conversion path. It is designed to make the value of content depth visible while keeping every demo boundary honest.

Success, in priority order:

1. The owner quickly understands the Business-tier value in the Beholden Coffee context.
2. The site feels complete and presentation-ready without implying that the concept page is official or accepting real inquiries.
3. The site establishes a reusable DDM handoff: owner sign-off, confirmed content, a real Formspree ID, and deployment to the client's own hosting and custom domain.

## Current demo boundary

- `index.html` is noindex and carries the unofficial concept-demo framing.
- The inquiry form is intercepted in `script.js`; no inquiry is submitted anywhere real.
- Menu prices and review content are presentation material and require owner confirmation before any paid launch.
- The visual asset boundary is exactly seven AI-generated concept images: pour-over bar, bean-selection ritual, coffee flight, Filipino sharing table, evening cocktails, Davao creamy mocha, and navy/amber texture. PNG/WebP pairs are alternate formats, not additional concepts.
- No scraped or client photography is included.

## Brand personality

Warm, grounded, sensory, and credible. The visual system uses the existing navy, amber, and cream tokens from `styles.css`; this document does not authorize new visual direction or content expansion.

## Hosting policy

Deploy the private noindex teaser demo to Vercel first for teaser/portfolio presentation, alternating to Netlify according to Netlify's monthly credit availability. Vercel is not the commercial production host for a paid client build while the account is on Hobby. Paid/converted client builds stay Netlify-only under DDM's standing rule for this project. After owner sign-off, the paid site moves to the client's own hosting and custom domain.

## Reusable operating model

Keep the implementation static and low-overhead: one HTML page, shared CSS/JS, existing image formats, platform config at the root, and a short owner sign-off checklist. Use `TEMPLATE-GUIDE.md` as the repeatable conversion and handoff SOP.
