# Section Archetypes

Date: 2026-04-23

## Purpose

Reusable section families for many projects.

These are not tied to a single brand. They are the company factory layer built on top of the Flatsome platform.

## Core archetypes

### Hero: slider + side CTA

- best for:
  - landing pages
  - campaigns
  - sales pages
- core stack:
  - `section`
  - `row`
  - `row_inner`
  - `ux_slider`
  - `ux_banner`
  - `text_box`
- variables:
  - slides
  - hero title
  - CTA copy
  - image IDs
  - overlay
  - height

### Hero: offset image + text card

- best for:
  - about
  - recruitment
  - service intros
- core stack:
  - `section`
  - `row`
  - `col`
  - `ux_banner`
  - `ux_text`
  - `button`
- variables:
  - image position
  - card offset
  - heading scale
  - background tone

### Gallery: staggered image strip

- best for:
  - brand storytelling
  - lifestyle pages
  - agency sites
- core stack:
  - `row_inner`
  - `col_inner`
  - `ux_banner`
  - `animate`
  - margin offsets
- variables:
  - image count
  - stagger depth
  - mobile stacking

### Feature grid

- best for:
  - benefits
  - services
  - differentiators
- core stack:
  - `row_inner`
  - `col_inner`
  - `ux_image`
  - `featured_box`
  - `ux_text`
- variables:
  - columns
  - icon/image style
  - border/depth
  - emphasis color

### Testimonials / proof band

- best for:
  - trust building
  - sales proof
  - employer branding
- core stack:
  - `section`
  - `testimonial`
  - `ux_text`
  - `divider`
- variables:
  - quote count
  - avatar or logo proof
  - dark/light mood

### CTA block

- best for:
  - conversion close
  - lead capture
  - next-step nudging
- core stack:
  - `section`
  - `ux_banner`
  - `text_box`
  - `button`
- variables:
  - background media
  - CTA button style
  - overlay strength

### Contact / signup section

- best for:
  - lead forms
  - contact pages
  - campaign capture
- core stack:
  - `section`
  - `row`
  - `ux_text`
  - `contact-form-7`
- variables:
  - form shortcodes
  - support text
  - split layout

### Content commerce / product block

- best for:
  - ecommerce
  - catalog landing
  - category discovery
- core stack:
  - `ux_products`
  - `ux_product_categories`
  - `ux_banner`
  - `ux_image_box`
- variables:
  - product source
  - columns
  - image hover
  - count

### Lookbook / hotspot story section

- best for:
  - editorial commerce
  - product storytelling
  - feature callout imagery
- core stack:
  - `section`
  - `row`
  - banner or image surface
  - hotspot interaction surface
  - optional product/story CTA
- variables:
  - image
  - hotspot count
  - callout labels
  - CTA destination

### Editorial posts / insights rail

- best for:
  - blog home
  - newsroom home
  - authority landing pages
- core stack:
  - `section`
  - `blog_posts`
  - title/text intro
  - optional slider behavior
- variables:
  - post source
  - card style
  - overlay
  - excerpt depth

### Footer block replacement

- best for:
  - reusable global footer systems
  - campaign-specific footer variants
  - multi-brand or multi-template operations
- core stack:
  - `block`
  - footer surface
  - widget/content groups
- variables:
  - block id
  - column structure
  - legal/support rows
  - proof/social layer

### Reusable header/content region block

- best for:
  - blog headers
  - shop headers
  - category headers
  - shared promo strips
- core stack:
  - `block`
  - `section`
  - nested native content modules
- variables:
  - block id
  - target surface
  - seasonal message
  - support CTA

### Contact split with map

- best for:
  - contact pages
  - office pages
  - service pages with local presence
- core stack:
  - `section`
  - `row`
  - `col`
  - `contact-form-7`
  - `map`
- variables:
  - form id
  - address copy
  - map height
  - map color/saturation
  - mobile stacking order

### Team roster grid

- best for:
  - about pages
  - leadership pages
  - recruitment pages
- core stack:
  - `section`
  - `row`
  - `team_member`
  - `ux_text`
- variables:
  - people count
  - card density
  - social/contact fields
  - image ratio

### Portfolio showcase rail

- best for:
  - agency home
  - case-study landing
  - creative or studio pages
- core stack:
  - `section`
  - `ux_portfolio`
  - `button`
  - optional `ux_text`
- variables:
  - project count
  - grid width
  - image height
  - CTA destination

### Tabbed FAQ / pricing panel

- best for:
  - pricing pages
  - FAQ pages
  - hybrid service explainer pages
- core stack:
  - `section`
  - `tabgroup`
  - `tab`
  - `accordion` or pricing rows
  - `button`
- variables:
  - tab count
  - tab style
  - pricing depth
  - FAQ category split

### Testimonial + logo proof rail

- best for:
  - trust sections
  - enterprise proof bands
  - service landing pages
- core stack:
  - `section`
  - `testimonial`
  - `logo`
  - `ux_slider` or row composition
- variables:
  - quote count
  - logo density
  - proof format
  - slider or static layout

### Video trigger banner

- best for:
  - story sections
  - process explainers
  - launch pages
- core stack:
  - `section`
  - `ux_banner`
  - `text_box`
  - `video_button`
- variables:
  - background media
  - trigger position
  - overlay strength
  - video destination

### Instagram / social proof strip

- best for:
  - social proof
  - visual commerce
  - lifestyle brand pages
- core stack:
  - `section`
  - `ux_instagram_feed`
  - `ux_text`
  - `divider`
- variables:
  - username or hashtag
  - photo count
  - columns
  - hover behavior

## Mapping rule

- archetype names are company-internal reusable labels
- implementation snippets should stay native Flatsome shortcodes
- project-specific copy belongs in the target project profile, not here
