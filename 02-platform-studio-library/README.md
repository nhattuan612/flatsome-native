# 02-platform-studio-library

Date: 2026-04-25

## Mục Đích

Đây là lớp thư viện Studio của Flatsome.

Nó dùng để:

- biết catalog Studio có gì
- biết category nào chứa loại UI nào
- biết effect và page setting nào đang có
- route nhanh từ template inventory sang native production

Library này tách thành 2 lớp:

- `data/flatsome-studio/*`
  - machine-readable truth
- `docs/superpowers/flatsome-native/02-platform-studio-library/*`
  - human-readable operating docs

## Đọc Gì Trước

1. `02-platform-studio-library/CATALOG-INDEX.md`
2. `02-platform-studio-library/Effects.md`
3. `02-platform-studio-library/Page Settings.md`
4. `categories/README.md`
5. các file category trong `02-platform-studio-library/categories/`

## Current Totals

- Visible Studio slots: `492`
- Unique template IDs: `337`
- Unique-only slots: `199`
- Canonical duplicate-group slots: `138`
- Duplicate slots: `155`
- Duplicate template IDs: `138`

## File Nào Làm Gì

- `02-platform-studio-library/CATALOG-INDEX.md`
  - index của catalog
- `02-platform-studio-library/Effects.md`
  - hiệu ứng đã hút được
- `02-platform-studio-library/Page Settings.md`
  - thông số page / container / width / layout
- `02-platform-studio-library/categories/`
  - inventory theo nhóm UI
- `categories/README.md`
  - hướng dẫn ngắn cho folder category

## Khi Nào Cập Nhật

- khi slot map thay đổi
- khi harvest thêm template
- khi phát hiện duplicate/unique cần sửa
- khi phát hiện effect hoặc page setting mới

## Regeneration

```bash
node scripts/ (ngoài hub) flatsome/flatsome_studio_build_slot_library.js
```

## Rules

- `01-platform/Native Builder Language Map.md` remains the shortcode-native language map
- category files track Studio inventory by visible slot
- duplicates are reconciled by `templateId`
- a slot is `canonical` when it is the first visible occurrence of a template in category traversal order
- source of truth của syntax không nằm ở folder này mà ở `01-platform/`
