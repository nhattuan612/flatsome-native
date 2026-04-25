# Flatsome Direct Harvest

## Mục tiêu

Hút toàn bộ catalog Flatsome Studio theo đường trực tiếp, không phụ thuộc UX Builder để khám phá template.

## Vì sao dùng hướng này

- nhanh hơn import qua UX Builder nhiều lần
- không bị kẹt UI canvas/iframe/overlay
- lấy được raw native content của template từ chính export endpoint
- dễ resume, dễ đo tiến độ, dễ chứng minh khi nào đạt 100%

## Nguồn dữ liệu

- home: `https://studio.uxthemes.com/`
- category pages: `https://studio.uxthemes.com/category/<id>/`
- export pages: `https://studio.uxthemes.com/export/<templateId>/`

## Kết quả lưu

- state: `VPS/data/flatsome-studio/harvest-state.json`
- catalog line-by-line: `VPS/data/flatsome-studio/catalog.ndjson`
- raw export từng template: `VPS/data/flatsome-studio/exports/<templateId>.json`

## Progress reporting

- gửi Telegram ở các mốc:
  - `RUN_START`
  - `CATEGORY_START`
  - `TEMPLATE`
  - `CATEGORY_DONE`
  - `FAIL`
  - `RUN_STOP`
  - `RUN_COMPLETE`

## Vai trò của UX Builder sau khi có direct harvest

- chỉ dùng để spot-check khả năng import thật vào WordPress
- không còn là đường chính để hút catalog
