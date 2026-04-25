# Overview And Source Rules

## Purpose

Internal reference for building `Flatsome UX Builder` pages in `shortcode-native` format instead of raw HTML.

## Dedupe Rule

- one shortcode = one primary entry
- add new evidence and parameters to the same entry
- do not duplicate the same shortcode under many page names
- Studio aliases such as `row_inner_1` and `col_inner_1` are evidence variants, not new layout primitives

## Operating Rule

For Flatsome work, prefer:

1. `section-first`
2. `ux-module-first`
3. `shortcode-native`
4. `page-local`
5. raw HTML only when native shortcode surface is not enough

## Delivery guardrail

- target `>=90%` native UX Builder modules
- do not use `ux_html` as the main layout engine
- visual similarity alone is not enough
- the page must remain editable in `UX Builder`

## What confirmed means

`Confirmed` means at least one of:

- shown in official UX Themes docs with working shortcode examples
- present in verified WordPress page content pulled from a real implementation environment

## Source layers

### Official UX Themes docs

- Docs home:
  - https://docs.uxthemes.com/
- Shortcodes:
  - https://docs.uxthemes.com/category/39-shortcodes
- Generate shortcode:
  - https://docs.uxthemes.com/article/223-how-to-generate-a-shortcode
- Blocks Custom Post Type:
  - https://docs.uxthemes.com/article/57-blocks-custom-post-type
- Lightbox shortcode:
  - https://docs.uxthemes.com/article/229-lightbox-shortcode
- Shop header with UX Builder:
  - https://docs.uxthemes.com/article/233-how-to-edit-shop-header-with-ux-builder
- Custom product page:
  - https://docs.uxthemes.com/article/245-how-to-create-a-custom-product-page
- Custom product page layout shortcodes:
  - https://docs.uxthemes.com/article/247-custom-product-page-layout-shortcodes
- Enable UX Builder for custom post types:
  - https://docs.uxthemes.com/article/221-how-to-enable-ux-builder-for-custom-post-types

### Official Flatsome demo surfaces

- UX Page Builder:
  - https://demos.flatsome.com/features/ux-page-builder/
- Elements overview:
  - https://demos.flatsome.com/features/elements-overview/
- Blocks element:
  - https://demos.flatsome.com/features/blocks-element/
- Header designer:
  - https://demos.flatsome.com/features/header-designer/
- Footer features:
  - https://demos.flatsome.com/features/footer-features/
- Blog features:
  - https://demos.flatsome.com/features/blog-features/
- Portfolio features:
  - https://demos.flatsome.com/features/portfolio-features/
- Elements surface family:
  - https://demos.flatsome.com/elements/

Use this layer to confirm:

- an element or surface is officially exposed by Flatsome
- a UI pattern is part of the intended operating surface
- a reusable page family exists in official demos

Do not use this layer alone to claim:

- full shortcode parameter coverage
- final syntax certainty for every element
- harvest-complete effect coverage

### Developer examples

- register custom shortcode in UX Builder:
  - https://gist.github.com/thinhbg59/d4dd63a76df4ac80fc355ae294b54a28
- custom post type + UX Builder setup pattern:
  - https://gist.github.com/webseo-onilne/6aaee7a04b33bf3a2f0a4903fa721c2f

### Verified implementation surfaces

- verified page extraction surfaces
- verified imported template surfaces
- `post_type=blocks` broad scan

## Extraction regex

Use the hyphen-aware shortcode regex:

```txt
/\[([a-zA-Z_][a-zA-Z0-9_-]*)/g
```

This prevents tags like `contact-form-7` from being collapsed incorrectly.
