# Flatsome 492-Slot Library Report

## Status

`PASS: slot-level Studio library built`

## What was built

- `492-slot` UI catalog map from public Flatsome Studio
- slot-level reconciliation to `337` unique `templateId`
- duplicate tracking by visible slot
- category-split Markdown library
- `02-platform-studio-library/Effects.md` and `02-platform-studio-library/Page Settings.md`
- `01-platform/Native Builder Language Map.md` linked to the new library system

## Final totals

- visible Studio slots: `492`
- unique template IDs: `337`
- unique-only slots: `199`
- canonical duplicate-group slots: `138`
- duplicate slots: `155`

## Output files

- `VPS/data/flatsome-studio/slot-map.ndjson`
- `VPS/data/flatsome-studio/slot-map-summary.json`
- `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/README.md`
- `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/CATALOG-INDEX.md`
- `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/categories/*.md`
- `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/Effects.md`
- `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/Page Settings.md`

## Notes

- `337 unique exports` from the earlier direct harvest are confirmed correct
- `492` is the visible slot count across Studio categories
- the difference is caused by cross-category duplication, now mapped explicitly at slot level

## Regeneration

```bash
node VPS/scripts/flatsome/flatsome_studio_build_slot_library.js
```

## Verify

```bash
node --test VPS/scripts/flatsome/flatsome_studio_build_slot_library.test.js
node VPS/scripts/flatsome/flatsome_studio_build_slot_library.js
wc -l VPS/data/flatsome-studio/slot-map.ndjson
```
