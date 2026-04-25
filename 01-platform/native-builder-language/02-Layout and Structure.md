# Layout And Structure

## Core layout primitives

### `section`

- Purpose: top-level section wrapper
- Minimal syntax:

```txt
[section label="Hero" padding="70px"]
  ...
[/section]
```

- Common parameters:
  - `label`
  - `padding`
  - `padding__sm`
  - `padding__md`
  - `margin`
  - `bg`
  - `bg_pos`
  - `bg_color`
  - `bg_overlay`
  - `dark`
  - `height`
  - `height__sm`

### `row`

- Purpose: primary row layout
- Minimal syntax:

```txt
[row style="collapse" width="full-width"]
  ...
[/row]
```

- Common parameters:
  - `label`
  - `style`
  - `width`
  - `custom_width`
  - `v_align`
  - `h_align`
  - `col_bg`
  - `col_bg_radius`
  - `padding`
  - `padding__md`

### `col`

- Purpose: primary column in a row
- Minimal syntax:

```txt
[col span="6" span__sm="12"]
  ...
[/col]
```

- Common parameters:
  - `span`
  - `span__sm`
  - `span__md`
  - `padding`
  - `padding__sm`
  - `padding__md`
  - `margin`
  - `margin__sm`
  - `margin__md`
  - `align`
  - `color`
  - `bg_color`
  - `bg_radius`
  - `depth`
  - `border`
  - `border_color`
  - `force_first`

### `row_inner`

- Purpose: nested row system inside a column
- Minimal syntax:

```txt
[row_inner width="custom" custom_width="100%"]
  ...
[/row_inner]
```

- Common parameters:
  - `style`
  - `col_style`
  - `width`
  - `custom_width`
  - `v_align`
  - `h_align`
  - `padding__md`

### `col_inner`

- Purpose: nested column inside `row_inner`
- Minimal syntax:

```txt
[col_inner span="4" span__sm="12"]
  ...
[/col_inner]
```

- Common parameters:
  - `span`
  - `span__sm`
  - `span__md`
  - `align`
  - `padding`
  - `margin`
  - `margin__sm`
  - `margin__md`
  - `bg_color`
  - `depth`
  - `border`
  - `border_color`
  - `animate`
  - `force_first`

## Structural helpers

### `page_header`

- Purpose: reusable page title/header block
- Minimal syntax:

```txt
[page_header style="simple" align="center" title="TUYEN DUNG"]
```

- Common parameters:
  - `style`
  - `align`
  - `title`
  - `title_size`
  - `title_case`
  - `nav_style`
  - `bg_color`
  - `bg_pos`

### `button`

- Purpose: CTA / link button
- Minimal syntax:

```txt
[button text="Ung tuyen ngay" color="secondary" style="underline"]
```

- Common parameters:
  - `text`
  - `color`
  - `style`
  - `radius`
  - `icon`

### `gap`

- Purpose: vertical spacing utility
- Minimal syntax:

```txt
[gap height="32px" height__sm="20px"]
```

- Common parameters:
  - `height`
  - `height__sm`
  - `height__md`

### `divider`

- Purpose: visual divider line
- Minimal syntax:

```txt
[divider align="center" width="150px" height="8px" color="rgb(254, 215, 80)"]
```

- Common parameters:
  - `align`
  - `width`
  - `height`
  - `margin`
  - `color`

## Evidence summary

- strong live evidence from verified extraction surfaces
- these primitives form the company default shell for all builder-safe layouts
