# Flatsome 492-Slot Library Implementation Plan

**Goal:** Build a slot-level Flatsome Studio catalog map that reconciles `492 visible UI slots` with `337 unique template exports`, then publish a maintainable Markdown library split by category.

**Why this exists**

- `catalog.ndjson` currently represents harvested unique exports
- the company still lacks a `UI slot -> templateId` truth table
- `01-platform/Native Builder Language Map.md` should remain the shortcode-native language map, not become an overloaded catalog dump

**Outputs**

- `data/flatsome-studio/slot-map.ndjson`
- `data/flatsome-studio/slot-map-summary.json`
- `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/README.md`
- `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/CATALOG-INDEX.md`
- `docs/superpowers/flatsome-native/02-platform-studio-library/categories/*.md`
- updated `VPS/docs/superpowers/flatsome-native/01-platform/Native Builder Language Map.md`

**Execution outline**

1. Audit the public Studio category counts and category pages.
2. Build a slot-map generator that captures every visible slot in category order.
3. Mark duplicates by `templateId` across categories.
4. Generate category Markdown files and an index from the slot map.
5. Link the library back into `01-platform/Native Builder Language Map.md`.
6. Verify totals:
   - visible slots
   - unique template IDs
   - duplicate slots
   - category totals
