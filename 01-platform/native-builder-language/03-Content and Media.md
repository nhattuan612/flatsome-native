# Content And Media

## Text and banner layer

### `ux_text`

- Purpose: text content block
- Minimal syntax:

```txt
[ux_text font_size="1.5"]
<h3>Heading</h3>
Body text
[/ux_text]
```

- Common parameters:
  - `font_size`
  - `font_size__sm`
  - `font_size__md`
  - `line_height`
  - `text_align`
  - `text_color`
  - `class`

### `ux_banner`

- Purpose: image/background banner block
- Minimal syntax:

```txt
[ux_banner height="550px" bg="402"]
  [text_box position_x="50" position_y="50"]
    <h3>Banner title</h3>
  [/text_box]
[/ux_banner]
```

- Common parameters:
  - `height`
  - `height__sm`
  - `height__md`
  - `bg`
  - `bg_color`
  - `bg_pos`

### `text_box`

- Purpose: overlay text container inside banner
- Minimal syntax:

```txt
[text_box position_x="50" position_y="50"]
  <h3>Title</h3>
[/text_box]
```

- Common parameters:
  - `position_x`
  - `position_y`
  - `width__sm`
  - `style`
  - `visibility`

## Image and card layer

### `ux_image`

- Purpose: image element
- Minimal syntax:

```txt
[ux_image id="545" width="20"]
```

- Common parameters:
  - `id`
  - `width`
  - `width__sm`
  - `width__md`

### `ux_image_box`

- Purpose: image + text card block
- Minimal syntax:

```txt
[ux_image_box img="11" image_height="90%" text_align="left"]
  ...
[/ux_image_box]
```

- Common parameters:
  - `img`
  - `image_height`
  - `image_hover`
  - `link`
  - `text_align`
  - `text_bg`
  - `text_color`
  - `text_padding`

### `featured_box`

- Purpose: feature/icon card
- Minimal syntax:

```txt
[featured_box img="288" img_width="50" pos="center"]
  <h3>Title</h3>
  Text
[/featured_box]
```

- Common parameters:
  - `img`
  - `img_width`
  - `pos`

## Slider, gallery, and media groups

### `ux_slider`

- Purpose: slider container
- Minimal syntax:

```txt
[ux_slider]
  [ux_banner ...]...[/ux_banner]
[/ux_slider]
```

### `ux_gallery`

- Purpose: gallery/media grid block
- Minimal syntax:

```txt
[ux_gallery ids="21028,21029,21030,21031" style="default" lightbox="false" columns__md="4" image_height="150%"]
```

- Common parameters:
  - `ids`
  - `style`
  - `lightbox`
  - `columns__md`
  - `image_height`
- Official demo value:
  - gallery and lightbox should be treated as related but separate operating surfaces

### `ux_banner_grid`

- Purpose: grid composition of banners/images
- Minimal syntax:

```txt
[ux_banner_grid spacing="xsmall" height="625" width="full-width"]
  [col_grid ...]...[/col_grid]
[/ux_banner_grid]
```

- Common parameters:
  - `spacing`
  - `height`
  - `width`

## Official demo confirmed media and interaction surfaces

These are officially present in Flatsome demo surfaces. Some still need direct shortcode capture before they can be treated as syntax-complete entries.

### `lightbox`

- Purpose: modal media/content reveal surface
- Minimal syntax:

```txt
[lightbox id="gallery-1" width="600px" padding="20px"]
  ...
[/lightbox]
```

- Status:
  - official demo confirmed
  - official shortcode doc exists
  - syntax shape confirmed at operating level
- Common parameters:
  - `id`
  - `width`
  - `padding`
- Operating value:
  - use when gallery/media needs focused click-through presentation without switching to raw HTML

### `hotspot`

- Purpose: clickable hotspot anchors over image/banner compositions
- Status:
  - official demo confirmed
  - syntax capture pending
- Operating value:
  - high-value for lookbook, product story, feature callout, and map-like image storytelling
- Current evidence:
  - official demo language confirms it can be combined with `banner`, `hotspot`, and `slider` surfaces
  - no direct `[hotspot ...]` shortcode has been captured yet in harvested Studio exports
- Working rule:
  - treat as `official surface + pattern value`
  - do not hand-author a shortcode entry until direct shortcode evidence exists

### `flip book`

- Purpose: image/card flip interaction surface
- Status:
  - official demo confirmed
  - syntax capture pending
- Operating value:
  - useful for product teaser, before/after, hover-reveal, and compact proof cards
- Current evidence:
  - official demo confirms the surface exists in Builder language
  - no direct shortcode has been captured yet in harvested Studio exports
- Working rule:
  - treat as `official presentational surface`
  - do not promote to syntax-complete until a real shortcode or official syntax doc is captured

### `video button`

- Purpose: play-trigger surface for opening a video or video-like interaction
- Minimal syntax:

```txt
[video_button video="https://www.youtube.com/watch?v=example"]
```

- Status:
  - official demo confirmed
  - harvested export confirms shortcode presence
- Common parameters:
  - `video`
- Operating value:
  - better native choice than custom HTML when the page only needs a trigger layer, not a custom embed shell

### `message box`

- Purpose: highlighted message / notice / inline promo box
- Status:
  - official demo confirmed
  - syntax capture pending
- Operating value:
  - useful for notice bars, promo callouts, disclaimers, and editorial emphasis blocks
- Current evidence:
  - official demo confirms the CTA/callout use case
  - no direct shortcode has been captured yet in harvested Studio exports
- Working rule:
  - treat as `official CTA/callout surface`
  - do not invent a shortcode entry until direct shortcode evidence exists

## Content blocks and surface modules

### `accordion`

- Purpose: collapsible FAQ / disclosure groups
- Minimal syntax:

```txt
[accordion]
  [accordion-item title="Question?"]
    <p>Answer</p>
  [/accordion-item]
[/accordion]
```

### `testimonial`

- Purpose: testimonial/review block
- Minimal syntax:

```txt
[testimonial]
  [gap height="1px"]
[/testimonial]
```

### `ux_stack`

- Purpose: stack-based layout helper
- Minimal syntax:

```txt
[ux_stack distribute="end" distribute__sm="start"]
  [button text="See all" color="secondary" style="underline"]
[/ux_stack]
```

- Common parameters:
  - `distribute`
  - `distribute__sm`
  - `gap`

### `title`

- Purpose: title element used in UX Blocks and layouts
- Minimal syntax:

```txt
[title style="center" text="Flatsome Main Features"]
```

### `logo`

- Purpose: logo / brand mark block
- Minimal syntax:

```txt
[logo img="136" height="60px"]
```

- Common parameters:
  - `img`
  - `height`
- Evidence:
  - harvested Studio exports

### `search`

- Purpose: search block / search form shortcode
- Minimal syntax:

```txt
[search style="flat"]
```

### `share`

- Purpose: share/social action block
- Minimal syntax:

```txt
[share]
```

## Evidence summary

- strongest evidence comes from imported Studio extraction surfaces
- these modules are the main layer for visuals without dropping into raw HTML
