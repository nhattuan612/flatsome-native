# Commerce And Dynamic

## Controlled fallback

### `ux_html`

- Purpose: raw custom HTML region when shortcode-native is not enough
- Rule:
  - allowed only when native shortcode surface is insufficient
  - never use as the main layout engine
  - company law still targets `>=90%` native modules

## Form and content embeds

### `contact-form-7`

- Purpose: embed a Contact Form 7 form inside a native Flatsome page
- Minimal syntax:

```txt
[contact-form-7 id="534"]
```

- Common parameters:
  - `id`
  - `title`

### `blog_posts`

- Purpose: posts/blog listing block
- Minimal syntax:

```txt
[blog_posts style="normal" columns="3" posts="6" show_date="text" image_height="56.25%"]
```

- Common parameters:
  - `style`
  - `columns`
  - `columns__md`
  - `slider_nav_style`
  - `slider_nav_position`
  - `slider_bullets`
  - `auto_slide`
  - `posts`
  - `show_date`
  - `image_height`
  - `text_align`
  - `text_bg`
  - `type`
  - `excerpt`
  - `col_spacing`

### `ux_instagram_feed`

- Purpose: Instagram feed block
- Minimal syntax:

```txt
[ux_instagram_feed username="sebdelaweb" photos="6" caption="0" columns="6" columns__md="3" hashtag="minimalinterior"]
```

- Common parameters:
  - `username`
  - `photos`
  - `caption`
  - `columns`
  - `columns__md`
  - `hashtag`

## Official demo confirmed utility and content surfaces

These surfaces are officially present in demo navigation and element pages. If syntax is not yet captured locally, keep them as confirmed surfaces rather than pretending the parameter map is complete.

### `forms`

- Purpose: native form presentation surface inside Flatsome page flows
- Status:
  - official demo confirmed
  - shortcode mapping not yet fully captured
- Operating value:
  - confirms a reusable form surface beyond raw embed fallback
  - official demo also indicates Contact Form 7 preset usage
  - current syntax-complete native embed in this hub remains `contact-form-7`

### `search box`

- Purpose: search input surface for header, content, or utility sections
- Status:
  - official demo confirmed
  - shortcode mapping still partial
- Operating value:
  - useful for knowledge base, shop discovery, and navigation-heavy pages

### `tabs`

- Purpose: segmented content surface for grouped information
- Minimal syntax:

```txt
[tabgroup style="line-bottom" align="center"]
  [tab title="New"]
    ...
  [/tab]
  [tab title="Sale"]
    ...
  [/tab]
[/tabgroup]
```

- Status:
  - official demo confirmed
  - harvested export confirms shortcode shape
- Common parameters:
  - `tabgroup`: `style`, `align`, `nav_size`
  - `tab`: `title`
- Operating value:
  - useful for FAQ, product details, process steps, and compact info architecture

### `map`

- Purpose: native map/location surface
- Minimal syntax:

```txt
[map height="540px" height__sm="340px" content_enable="0" color="#455e61" saturation="-81"]
  <h3>Address</h3>
  <p>Support copy</p>
[/map]
```

- Status:
  - official demo confirmed
  - harvested export confirms shortcode shape
- Common parameters:
  - `height`
  - `height__sm`
  - `lat`
  - `long`
  - `zoom`
  - `content_enable`
  - `content_bg`
  - `content_width`
  - `content_width__sm`
  - `content_width__md`
  - `position_x__sm`
  - `position_y__sm`
  - `color`
  - `saturation`
- Operating value:
  - preferred before falling back to `ux_html` iframe embed

### `price table`

- Purpose: pricing comparison surface
- Status:
  - official demo confirmed
  - no dedicated shortcode confirmed in harvested exports
- Operating value:
  - useful for service pricing, package comparison, and membership tiers
  - currently treated as a native composition pattern built from `tabgroup`, `row`, `featured_box`, `divider`, lists, and `button`

### `team member`

- Purpose: people/team profile card surface
- Minimal syntax:

```txt
[team_member img="21247" name="Ola Nordmann" title="CEO and Founder" icon_style="small" facebook="#" phone="#" linkedin="#" image_height="100%" image_width="80" image_radius="100"]
[/team_member]
```

- Status:
  - official demo confirmed
  - harvested export confirms shortcode shape
- Common parameters:
  - `img`
  - `name`
  - `title`
  - `icon_style`
  - `facebook`
  - `phone`
  - `linkedin`
  - `image_height`
  - `image_width`
  - `image_radius`
- Operating value:
  - useful for about, leadership, experts, and recruitment pages

### `portfolio`

- Purpose: project/case-study listing surface
- Minimal syntax:

```txt
[ux_portfolio number="4" type="row" columns="2" image_height="75%"]
```

- Status:
  - official demo confirmed
  - harvested export confirms shortcode shape
- Common parameters:
  - `number`
  - `type`
  - `columns`
  - `image_height`
- Operating value:
  - confirms Flatsome supports a reusable showcase surface outside blog and products
  - official features also confirm filter navigation, slider/grid layouts, and lightbox-oriented presentation

### `logo`

- Purpose: logo/brand mark surface
- Status:
  - official demo confirmed
  - syntax captured in content/media layer as `[logo ...]`
- Operating value:
  - useful for partner bars, trust strips, and client proof sections

## Commerce blocks

### `ux_product_categories`

- Purpose: product-category listing block
- Minimal syntax:

```txt
[ux_product_categories style="default" type="row" columns="3" columns__sm="1" number="3" show_count="0" image_height="56.25%"]
```

### `ux_products`

- Purpose: product listing / product grid block
- Minimal syntax:

```txt
[ux_products style="normal" type="row" columns__sm="2" columns__md="2" products="4" image_height="100%" text_bg="rgb(255, 255, 255)"]
```

### `ux_pages`

- Purpose: page grid/listing block
- Minimal syntax:

```txt
[ux_pages style="default" parent="3021" columns="3" text_align="center"]
```

- Official demo value:
  - confirms `pages` as a real reusable listing surface, not just a fallback content query

### `ux_countdown`

- Purpose: countdown element
- Minimal syntax:

```txt
[ux_countdown]
```

### Official demo implications for commerce surfaces

- `ux_product_categories` is a first-class discovery surface, not only a shop archive helper
- `ux_products` is used both as grid and slider-oriented merchandising surface
- `blog_posts`, `ux_products`, and `ux_product_categories` can all act as section-level content engines inside native page composition
- `blog_posts` should be treated as a flexible engine with slider, row, grid, and masonry-style use cases

## Reusable content pattern

### `block`

- Purpose: reuse a saved UX Block in other places
- Typical syntax:

```txt
[block id="123"]
```

- Use:
  - convert repeated company sections into reusable library units

## Evidence summary

- strongest evidence surfaces:
  - verified page extraction
  - verified imported template extraction
  - broad scan of `post_type=blocks`
