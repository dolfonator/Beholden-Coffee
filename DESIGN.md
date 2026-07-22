# Beholden Coffee Visual System

## 1. Overview

Beholden Coffee is a friendly and approachable local coffeehouse teaser-demo. It should feel warm, familiar, and easy to choose, not formal luxury. The visual language uses coffee ink, warm section bands, navy evening fields, honey highlights, and clear local-business calls to action.

This is a Business-tier teaser-demo. It demonstrates the richer paid-site direction with a complete menu, specialties, gallery, reviews, visit information, map fallback, and inquiry form. It is not the final signed-off production site and must not imply confirmed brand assets, photography, prices, reviews, or business claims.

The system inherits the grounded-panel architecture from the DDM Business template. Panels are used where content needs physical emphasis: body copy, menu boards, cards, contact information, forms, map surfaces, and hero copy. Section bands remain open and use typography, spacing, and a quiet numeral to provide structure.

## 2. Palette

| Token | Color | Role |
| --- | --- | --- |
| Brand amber | `#E8A200` | **PROVISIONAL.** Honey amber for identity and restrained accent use only. It is inferred from the brand's bee and honey motif, not sampled from an official logo. Correct it when real brand files arrive. |
| Action brown | `#8A5B00` | WCAG-AA-safe text color for links, prices, quiet actions, and text on light or white backgrounds. |
| Brand navy | `#1D2F3A` | Primary navy field, dark panel surface, and primary button background. |
| Deep navy | `#13232D` | Dark section fields, footer, review room, and deep scrim tone. |
| Warm cream | `#FFF8E8` | Lightest section band and warm page surface. |
| Menu cream | `#F5EAD5` | Medium warm band, panel wash, and soft utility surface. |
| Pale oak | `#EAD7B5` | Deepest warm band, secondary light-on-dark copy, and grounded dividers. |
| Coffee ink | `#32261F` | Primary text on light surfaces. |
| Soft ink | `#62584E` | Secondary text on light surfaces. |
| Tropical green | `#4F6B58` | Restrained accent only, used sparingly for specialty or nature cues. |
| Panel surface | `#FFFCF5` | Light card, menu, contact, and form surface. |
| Honey highlight | `#F5C451` | Highlight, star, focus, and accent text on navy backgrounds only. |

### Color rules

- The provisional amber identifies Beholden. Do not use `#E8A200` for small or body text on white or near-white backgrounds.
- Use `#8A5B00` for action, link, and price text on light surfaces.
- Use white or warm cream copy on the navy tones. Use honey highlight text only on navy backgrounds.
- Use coffee ink for primary light-surface copy and soft ink for secondary copy.
- Shadows are tinted toward coffee ink or navy and stay limited to real objects.

## 3. Typography

The existing two-typeface pairing is retained exactly:

- **Display and headings:** Fraunces, with Iowan Old Style and Georgia fallbacks.
- **Body and UI:** Hanken Grotesk, with system UI fallbacks.

Fraunces carries the welcoming display voice. Hanken Grotesk keeps navigation, labels, prices, form fields, contact details, and supporting copy practical and readable. The `PesoFix` codepoint shim remains scoped to the peso sign so menu prices render correctly without changing the type pairing.

## 4. Logo and wordmark

Only a text wordmark is used for Beholden Coffee. Do not fabricate or introduce a logo image, badge, bee mark, or other invented brand asset. The wordmark uses Fraunces for the name and Hanken Grotesk for any supporting descriptor.

## 5. Layout and components

### Grounded panels

The inherited grounded-panel system is the main structural rule. Panels use the shared radius, border, spacing scale, and tinted shadow. Light panels use `#FFFCF5`; dark panels use the navy tokens. Accent bars are sparing and should mark a real content object, not decorate every section.

### Hero

The hero uses `assets/hero-pour-over-bar.webp` with a deliberate deep-navy scrim. Copy sits inside a semi-transparent navy grounded panel so the headline, supporting text, and actions do not float directly on the photo. Primary actions use navy with light text. Secondary actions use a visible light outline.

### Specialties

The specialties or flavor-card grid is designed for exactly three cards: Coffee Ritual, Filipino Kitchen, and Cocktails After Dark. It uses three balanced columns on wide screens, two columns at the existing medium breakpoint, and one column on narrow screens.

### Menu, gallery, reviews, visit, and form

- The menu remains a tactile panel with clear category headings, dotted leaders, and action-brown prices.
- Gallery tiles use the approved concept-image set and retain the existing responsive 2-up to 1-up grid.
- Reviews remain in a deep-navy section with navy cards, warm light copy, honey stars, and explicit placeholder disclosure.
- Visit keeps the contact card and map card as usable grounded panels. `.map-embed` contains the iframe, while `.map-fallback` provides the address and Google Maps link behind it if the embed is unavailable.
- The form remains a light panel with readable labels, fields, helper copy, and a visible action focus ring.

## 6. Image-source boundary

The only approved image sources for this teaser-demo are these seven AI-generated concept images:

1. `assets/hero-pour-over-bar.webp`
2. `assets/bean-selection-ritual.webp`
3. `assets/coffee-flight.webp`
4. `assets/davao-creamy-mocha.webp`
5. `assets/filipino-sharing-table.webp`
6. `assets/evening-cocktails.webp`
7. `assets/navy-amber-texture.webp`

Do not scrape images from the web. Do not use client photography. Do not imply that concept images depict confirmed products, interiors, staff, or services. Replace them only when approved real brand files and usage rights are available.

## 7. Accessibility and motion

- Maintain the existing native scrolling, keyboard focus treatment, responsive breakpoints, and grounded panel hierarchy.
- Keep body text at WCAG AA contrast or better. Action brown is the light-surface text color; navy and honey combinations are reserved for dark fields.
- Preserve `prefers-reduced-motion: reduce`: reveal content is static, hover movement is disabled, and animated transitions are removed.
- Keep the layout usable at 320px without horizontal overflow. Buttons, menu rows, contact links, map fallback content, and form fields must remain reachable and readable.

## 8. Do and do not

### Do

- Keep the direction friendly, approachable, grounded, and specific to a coffeehouse.
- Use the approved palette through the CSS token surface.
- Reuse the grounded-panel system and existing spacing scale.
- Keep the Business teaser-demo status and concept-image boundary explicit.

### Do not

- Do not present the provisional amber as an official sampled logo color.
- Do not use amber for small text on light backgrounds.
- Do not add a fabricated logo image or bee illustration.
- Do not use scraped or client photography.
- Do not turn the teaser-demo into a formal luxury coffee brand or expand beyond the approved visual system.
