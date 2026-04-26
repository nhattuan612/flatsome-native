# Flatsome Direct Harvest Report

## Trạng thái

`PASS: full direct harvest completed`

## Script

- `scripts/ (ngoài hub) flatsome/flatsome_studio_direct_harvest.js`
- `scripts/ (ngoài hub) flatsome/flatsome_studio_direct_harvest.test.js`

## Đặc tính đã có

- parse category trực tiếp từ Flatsome Studio home
- parse template cards từ category pages
- fetch export payload từ từng `templateId`
- lưu raw export cục bộ
- resume bằng state file
- dedupe theo `templateId`
- Telegram notify theo category/template/fail/run status

## Verify local

- `node --test scripts/ (ngoài hub) flatsome/flatsome_studio_direct_harvest.test.js`
- `node --check scripts/ (ngoài hub) flatsome/flatsome_studio_direct_harvest.js`

## Kết quả

- hoàn tất `19` category
- hoàn tất `337` template export
- `0` fail
- raw export files:
  - `337` file trong `data/flatsome-studio/exports (ngoài hub)`
- catalog index:
  - `337` dòng trong `data/ (ngoài hub) flatsome-studio/catalog.ndjson`

## Mốc cuối

- category cuối:
  - `Wireframes`
- template cuối:
  - `15278` `Hero Banner 1`
- thời điểm cuối:
  - `2026-04-23T03:45:56.887Z`

## Dữ liệu đầu ra

- state:
  - `data/ (ngoài hub) flatsome-studio/harvest-state.json`
- catalog:
  - `data/ (ngoài hub) flatsome-studio/catalog.ndjson`
- exports:
  - `data/flatsome-studio/exports (ngoài hub)/*.json`

## Kết quả mong muốn

- hút 100% template export mà không cần thao tác UX Builder
- dùng dữ liệu này để cập nhật `01-platform/Native Builder Language Map.md`
