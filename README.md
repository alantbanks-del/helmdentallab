# Helm Dental Laboratory — CHROME GuidedSMILE

Co-branded landing page for CHROME GuidedSMILE at Helm Dental Laboratory
(Digital Esthetic Solutions), Wylie TX.

Single self-contained `index.html`. Styles, scripts, and images — including the
Helm logo — are inlined. No build step, no dependencies.

## Deploy

Netlify: connect this repo, leave the build command empty, publish directory `/`.
Push to `main` and it redeploys. `index.html` sits at the repo root.

## Notes

Product slides are hotlinked from `guidedsmile.netlify.app`. Fonts load from
Google Fonts. Everything else, logo included, is embedded in the HTML.

Content is drawn from helmdentallaboratory.com: 972-442-9772 ·
info@helmdentallaboratory.com · 2801 Capital Street, Wylie TX 75098 · Tulsa second
location · Doctor Portal, RX Forms, File Upload, TikTok/Facebook/Instagram.

**Framing: existing capability, not an introduction.** Helm's live site has a
dedicated CHROME page describing them as *"the original exclusive lab provider in
Texas for CHROME GuidedSMILE."* That claim leads the hero. Their own five-stage
anchored description (bite verification, bone reduction, site drilling,
provisionalization, transfer to conversion) drives the tiles and the panel. They
also run coDiagnostiX and Simplant, reflected in the stats and copy.

The logo is Helm's real brand mark (HDL + Digital Esthetic Solutions lockup),
supplied by the client. Full-colour lockup in the header; a white-knockout of the
Helm mark in the footer so it stays legible on the dark background.

Copy is written uniquely for this lab. Product names, the shared headline, and
Helm's own site terminology repeat as they should, but no invented prose is shared
with the other partner pages.

## Don't undo these

**`.hero { padding: 0 }`** — `section { padding: 84px 0 }` is global and the hero
*is* a `<section>`. Remove the override and ~170px of dead space appears.

**The reveal class is `is-vis`, not `in`** — `.hero .in` is a flex container.

**No `object-fit: cover` on `.shot img`** — the product slides are 16:9 with text
near the edges. Cropping cuts words off.

## Colors

| Token | Hex | Use |
|---|---|---|
| `--navy` | `#1e2a44` | headings, dark sections |
| `--crim` | `#a6284b` | accent, buttons |
| `--crim-lt` | `#e88aa3` | accent on dark only |
| `--muted` | `#5c616e` | body text |

Crimson sampled from Helm's own logo (`~#a6284b`); navy from the Digital Esthetic
Solutions sub-brand. Every text/background pair measured — zero WCAG AA failures
across 17 pairs. Crimson passes both directions: 6.61:1 on light, 6.94:1 white-on.

Type: Oswald (condensed, for headings and the industrial feel their brand carries)
over Source Sans 3 for body.
