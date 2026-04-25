# Patterns And Workflow

Date: 2026-04-25

## Mục Đích

File này chỉ giữ:

- verified native pattern archetypes
- high-value pattern meaning cho authoring

File này không còn giữ:

- extraction workflow
- browser snippet workflow
- worker capability note

Các phần đó đã được tách sang:

- `05-flows/Imported Template Extraction Flow.md`
- `05-flows/Execution Role Boundaries.md`

## Verified shortcode pattern archetypes

### Pattern: Slider hero + side CTA

- Live evidence:
  - verified native page extraction
- Core stack:
  - `row`
  - `col`
  - `row_inner`
  - `col_inner`
  - `ux_slider`
  - `ux_banner`
  - `text_box`
  - `section`

### Pattern: Offset image hero

- Live evidence:
  - verified native page extraction
- Core stack:
  - `section`
  - `row`
  - `col`
  - `ux_banner`
  - `ux_text`
  - `button`

### Pattern: Image strip / staggered gallery

- Live evidence:
  - verified native page extraction
- Core stack:
  - `row_inner`
  - `col_inner`
  - `ux_banner`
  - `animate`
  - margin offsets

### Pattern: Feature grid

- Live evidence:
  - verified native page extraction
- Core stack:
  - `row_inner`
  - `col_inner`
  - `ux_image`
  - text/html
  - `featured_box`

### Pattern: Recruitment hero with simple page header

- Live evidence:
  - verified native page extraction
- Core stack:
  - `section`
  - `gap`
  - `page_header`
  - `ux_banner`
  - `text_box`

### Pattern: Imported Studio mega-template page

- Live evidence:
  - verified imported template extraction
- Meaning:
  - high-value source for discovering native shortcode vocabulary faster than docs alone

### Pattern: Lookbook / hotspot storytelling section

- Live evidence:
  - official demo surface confirmation
- Core stack:
  - banner or image surface
  - hotspot interaction layer
  - optional slider or product/story callouts
- Meaning:
  - high-value native pattern for editorial commerce and visual storytelling without custom HTML shells

### Pattern: Footer replacement via reusable block

- Live evidence:
  - official demo feature confirmation
- Core stack:
  - `block`
  - footer replacement surface
  - widget/footer composition
- Meaning:
  - confirms footer should be treated as a reusable native operating surface, not as a one-off static layout

### Pattern: Reusable block as blog/shop/category header surface

- Live evidence:
  - official demo feature confirmation
- Core stack:
  - `block`
  - custom blog header
  - custom shop header
  - shop category header
- Meaning:
  - confirms `block` is not only a reusable section primitive, but also an operating surface for large shared page regions

### Pattern: Editorial posts slider / teaser rail

- Live evidence:
  - official demo feature and element confirmation
- Core stack:
  - `blog_posts`
  - slider behavior
  - banner/image-driven preview cards
- Meaning:
  - useful for magazine, insights, newsroom, and authority-style homepages
  - official demo confirms slider, row, grid, and masonry-style behaviors for the same content engine

### Pattern: Shop hero + category discovery band

- Live evidence:
  - official shop demo confirmation
- Core stack:
  - hero banner or slider
  - `ux_product_categories`
  - `ux_products`
- Meaning:
  - confirms category discovery is part of the primary page composition language, not just archive navigation

### Pattern: Utility section with message/search/form surface

- Live evidence:
  - official element confirmation
- Core stack:
  - `search box`
  - `forms`
  - `message box`
  - `ux_text`
- Meaning:
  - good for help center, conversion capture, and utility-focused landing pages

## Studio library system

Separate Studio catalog library:

- `02-platform-studio-library/README.md`
- `02-platform-studio-library/CATALOG-INDEX.md`
- `02-platform-studio-library/categories/`

This split matters:

- `01-platform/Native Builder Language Map.md` = builder language and authoring logic
- `02-platform-studio-library/*` = Studio inventory by visible UI slot

## File Liên Quan

- `05-flows/Imported Template Extraction Flow.md`
- `05-flows/Execution Role Boundaries.md`
