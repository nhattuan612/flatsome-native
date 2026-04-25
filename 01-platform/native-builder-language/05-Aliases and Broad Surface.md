# Aliases And Broad Surface

## Imported Studio alias patterns

These are valid evidence, but should not be treated as the main authoring surface.

### `col_grid`

- Purpose: grid-style column helper seen in imported Studio content
- Minimal syntax:

```txt
[col_grid span="3" span__sm="12" span__md="6" height="2-3"]
  [ux_banner ...]...[/ux_banner]
[/col_grid]
```

### `row_inner_1`

- Purpose: imported alias/nested-row variant
- Rule:
  - treat as Studio-generated alias
  - do not use as the default authoring primitive

### `col_inner_1`

- Purpose: imported alias/nested-column variant
- Rule:
  - treat as Studio-generated alias
  - do not use as the default authoring primitive

## Broad page-scan shortcodes

These are not primary Flatsome-native layout primitives, but they appear on live pages and matter for total surface awareness.

- `woocommerce_cart`
- `woocommerce_checkout`
- `woocommerce_my_account`
- `woocommerce_order_tracking`
- `yith_wcwl_wishlist`

## Official demo confirmed broad surface rule

Not every official element needs to be promoted into a full syntax entry immediately.

When official demo evidence confirms a surface but local shortcode capture is still incomplete:

- keep it in the knowledge hub as `officially confirmed`
- mark it `syntax capture pending`
- do not invent missing parameters
- promote it to a full syntax entry only after direct shortcode evidence is captured

## Developer-side APIs

These are not page shortcodes. They are developer hooks and functions for extending what appears in UX Builder.

### `add_ux_builder_shortcode(...)`

- Purpose: register a custom shortcode so it appears in UX Builder
- Status:
  - developer example found
  - not yet validated in this project repo/server code

### `add_ux_builder_post_type(...)`

- Purpose: enable builder support or custom builder behavior for post types
- Status:
  - developer gist evidence
  - official doc exists
