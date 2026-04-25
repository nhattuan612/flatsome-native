# Flatsome Shortcode-Native Operating Model

Date: 2026-04-22

## Decision

The company standard for new Flatsome work is now:

- `section-first`
- `ux-module-first`
- `shortcode-native`
- `page-local`
- raw HTML only when Flatsome shortcode/native surface is not enough

For product page delivery, this also means:

- target `>=90%` native UX Builder modules by structure
- do not build the page as a large `ux_html` shell
- HTML is acceptable only inside native text-capable modules or for minimal link/embed edge cases
- the final output must remain editable in `UX Builder` as real blocks, rows, columns, sliders, banners, buttons, stacks, titles, dividers, testimonials, and related native modules

This means Codex should prefer writing in Flatsome's own builder language:

- `[section]`
- `[row]`
- `[col]`
- `[ux_text]`
- `[ux_banner]`
- `[button]`
- `[ux_image]`
- `[ux_slider]`
- `[featured_box]`
- `[gap]`

instead of defaulting to plain HTML.

## Current intake gate

Mọi task mới không được nhảy thẳng từ brief sang build.

Chuỗi vào cửa chuẩn hiện tại là:

`Quick Start Menu -> Guided Intake Questions -> Input Contract -> Brief Intake Flow -> Page Plan`

Điều này tồn tại để khóa đúng:

- loại input
- output expectation
- style source
- reference authority

## Why this model

- Keeps the current Flatsome stack in place
- Lets Codex work faster and more deterministically than freeform dragging
- Keeps the final page editable in UX Builder for later drag-drop changes
- Minimizes migration cost and reduces dependence on fragile visual automation
- Prevents the false success case where the page looks correct but is actually just HTML trapped inside Builder

## How Codex will learn Flatsome native structure

Codex does **not** need to memorize the entire Flatsome shortcode surface up front.

The correct learning model is:

1. Extract shortcode output from real existing pages
2. Map each repeated design pattern to its native shortcode structure
3. Build a company section library from those working patterns
4. Reuse and adapt proven blocks instead of inventing from scratch each time

## Operating knowledge sources

Priority order:

1. Existing verified native patterns already confirmed in the company map
2. Flatsome page content / shortcode output from WordPress editor
3. Reusable internal snippets collected from successful sections
4. Targeted reference lookup only when a needed shortcode pattern is still unknown

## Platform rule

Project-specific websites may be used as temporary validation surfaces, but they must not define the platform.

Reusable knowledge must stay domain-agnostic first.

## Practical workflow for future Flatsome tasks

For a new page:

1. Audit an existing page with similar layout
2. Extract native Flatsome shortcode patterns from the page content
3. Recompose into a new page using:
   - native sections
   - rows
   - columns
   - banners
   - text blocks
   - buttons
   - spacing blocks
4. Prefer native module substitution over custom CSS/HTML when a visual issue appears
5. Save on the page-local surface
6. Open in UX Builder and confirm the result is editable as native blocks
7. Verify on the public URL
8. Run edit-surface verification
9. Run builder-surface verification
10. Record final verification evidence before claiming completion

## Product delivery rule

For a delivered Flatsome page, Codex should assume this quality bar by default:

1. `ux_html` should be `0` unless there is a documented exception
2. layout should be built from native Flatsome modules first
3. if an asset/module renders poorly, replace it with a better native module rather than falling back to raw layout HTML
4. remove fake in-page footer/header sections if they conflict with the real site chrome
5. completion claims require fresh verification evidence from:
   - public page
   - edit page
   - UX Builder page
   - final verification artifact

## Company asset to build over time

Codex should gradually maintain a reusable internal library of:

- hero sections
- about sections
- feature grids
- CTA sections
- image rows
- stats / icon boxes
- team sections
- testimonial sections
- contact sections
- ecommerce sections
- blog teaser sections

Each entry should contain:

- the shortcode snippet
- the purpose
- optional variables to change:
  - title
  - subtitle
  - image IDs
  - button text
  - button links
  - spacing
  - colors

## Management rule

OpenClaw is not responsible for inventing Flatsome layouts.

OpenClaw may help with:

- opening the correct admin/page surface
- basic verification
- operational reporting

Codex remains responsible for:

- deciding the page structure
- authoring shortcode-native output
- quality control
- final verification

## Immediate implication

Future Flatsome page requests should be executed in this order:

1. find the closest native pattern
2. author shortcode-native output with native modules first
3. keep the result editable in UX Builder
4. verify `public + edit + builder`
5. avoid raw HTML unless native shortcode is insufficient
