# Composition Rules

Date: 2026-04-23

## Purpose

Provide repeatable assembly logic so a new page can be built quickly without redesigning structure from zero.

## Assembly rules

1. start `section-first`
2. choose page goal before choosing visuals
3. route brief through `03-factory/Page Goal Routing.md` before writing `Section Map`
4. compose from archetypes, not from raw shortcode fragments
5. keep output `shortcode-native`
6. only fall back to raw HTML where native surface is not enough
7. decide `reuse existing block / create new / page-only block` before writing full `Section Map`

## Standard page skeletons

### Landing page

1. hero
2. trust/proof
3. feature grid
4. image/content split
5. CTA close

### About page

1. intro hero
2. story/content split
3. values/features
4. team or process
5. CTA/contact

### Recruitment page

1. headline hero
2. culture/value blocks
3. open positions or benefits
4. testimonial/proof
5. form CTA

### Ecommerce landing

1. campaign hero
2. categories
3. featured products
4. benefits/proof
5. CTA / newsletter / blog teaser

### Editorial / blog homepage

1. headline hero
2. featured posts rail
3. category/topic discovery
4. authority/proof strip
5. newsletter or CTA close

Notes:
use `blog_posts` as a flexible engine, not only as a default post grid; official demo confirms slider, row, grid, and masonry-like uses

### Lookbook / visual story page

1. hero image or banner
2. hotspot storytelling section
3. supporting product or content band
4. proof / editorial note
5. CTA close or discovery rail

### Contact page

1. intro hero
2. contact split with map
3. support/contact details row
4. FAQ or reassurance strip
5. CTA or footer proof close

### Portfolio / case-study landing

1. hero
2. portfolio showcase rail
3. service/process strip
4. testimonial + logo proof rail
5. CTA close

### Service / agency page

1. hero
2. feature grid
3. portfolio showcase rail or proof band
4. team roster or process
5. contact split with map or CTA close

### Pricing / FAQ page

1. intro hero
2. tabbed pricing / FAQ panel
3. proof strip
4. service/support clarifier
5. conversion close

## Variation rules

- vary `content`, not platform syntax
- vary `spacing`, `color`, `image IDs`, `overlay`, `animation`, and `section order`
- use Studio catalog for inspiration
- use official demo surfaces to validate whether a pattern already exists natively
- keep each section independently editable inside UX Builder
- choose archetype by `page goal` first, then by visual tone
- if a section is mostly about trust, prefer `testimonial + logo proof rail` before inventing a custom trust layout
- if a section is mostly about structured comparison, prefer `tabbed FAQ / pricing panel` before building ad-hoc columns
- if a section is mostly about team or people credibility, prefer `team roster grid` before composing image cards from scratch
- if an archetype already maps to a `P1` block candidate, default to reuse-first and force a written reason if choosing create-new

## Anti-patterns

- writing project-specific copy into platform docs
- treating one live site as the default design language
- collapsing large pages into raw HTML when native shortcodes can do the job
- recreating reusable proof/contact/team sections from scratch when a stable archetype already exists
