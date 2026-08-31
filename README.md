# Structure Studies

Three landing pages rebuilt section-for-section from sites whose structure I admire. Each one keeps the exact section order and layout logic of the reference, then swaps in a new brand, new copy, and new imagery.

| Page | Reference | Concept |
|---|---|---|
| [`/foyer`](foyer/index.html) | luma.com | Foyer - a gatherings platform. Floating poster tiles around a rotating headline, one CTA, closing band, footer. |
| [`/foyer-v2`](foyer-v2/index.html) | luma.com | Foyer v2 - the same structure rebuilt in the WDLP design system (navy / electric / paper, Clash Display + Geist Mono + Instrument Serif italics, 8px radius, GSAP reveals and parallax, navy closing container framing a product preview). Reuses `/foyer/img`. |
| [`/maya-iyer`](maya-iyer/index.html) | arthurbrooks.com | Dr. Maya Iyer - a sleep scientist's personal brand. Hero carousel, testimonial carousel, quiz band, crisis-to-solution arc, podcast, books, speaking, partnerships, membership, signup footer. |
| [`/harbor`](harbor/index.html) | calendly.com | Harbor - a client-ops SaaS for freelancers. Product tabs, four-step process, four accordion feature blocks, customer stories, integrations, get-started, marquee, footer. |

The hub at `/` links all three.

## Rules the pages follow

- Section order and layout roles match the reference 1:1. Nothing added, nothing dropped.
- Every word, colour, and brand is original. No copy is reused from the references.
- Solid flat colours only. No gradients, no glow effects (the reference sites' gradient panels became flat solids).
- One self-contained `index.html` per page: inline CSS and JS, inline SVG icons, no libraries.
- Type: Haffer (local) with Geist and Inter as web fallbacks; Newsreader and Instrument Serif where the reference uses a serif.
- Responsive to 375px. Every interactive element (carousels, tabs, accordions, rotating words, marquee) actually works.

## Imagery

All photos and poster art were generated with [Higgsfield](https://higgsfield.ai):

- Foyer tiles: GPT Image 2, rendered as four 2x2 poster grids and sliced.
- Maya Iyer: one GPT Image 2 portrait as the identity anchor, then Nano Banana Pro with that portrait as a reference for every other scene, so the same person appears across the page.
- Harbor: GPT Image 2 for the customer and marquee photos.

Product mockups, book covers, and the phone are built in CSS.

## Layout

```
index.html          hub
assets/             hub thumbnails
foyer/              page + img/tile-01..16.jpg, community-1..6.jpg
foyer-v2/           WDLP-system variation of Foyer (shares /foyer/img)
maya-iyer/          page + img/hero-1..5, testimonial, portrait, podcast, speaking, partnership
harbor/             page + img/story-1..5, marquee-1..4
vercel.json         cleanUrls
```

## Running locally

Open any `index.html` directly, or `npx serve .` from the repo root for clean URLs.

## Credits

Reference sites belong to their owners. These are structural studies for my portfolio. Built by [Hardik Dewra](https://wedesignlandingpages.com), 2026.
