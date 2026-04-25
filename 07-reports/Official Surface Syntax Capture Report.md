# Official Surface Syntax Capture Report

Date: 2026-04-24

## Trạng thái

`PASS: syntax capture completed where evidence is strong`

## Nguồn bằng chứng

### Official docs

- https://docs.uxthemes.com/article/229-lightbox-shortcode

### Harvested exports

- `VPS/data/flatsome-studio/exports/3732.json`
- `VPS/data/flatsome-studio/exports/274.json`
- `VPS/data/flatsome-studio/exports/15409.json`
- `VPS/data/flatsome-studio/exports/16953.json`
- `VPS/data/flatsome-studio/exports/16773.json`
- `VPS/data/flatsome-studio/exports/590.json`

## Surface đã lên mức syntax-complete

### `lightbox`

- nguồn chính: official docs
- trạng thái: syntax shape confirmed

### `video_button`

- nguồn chính: harvested export
- syntax:
  - `[video_button video="https://www.youtube.com/watch?v=example"]`

### `logo`

- nguồn chính: harvested export
- syntax:
  - `[logo img="136" height="60px"]`

### `map`

- nguồn chính: harvested export
- syntax:
  - `[map height="540px" height__sm="340px" ...] ... [/map]`

### `tabgroup` + `tab`

- nguồn chính: harvested export
- syntax:
  - `[tabgroup ...] [tab title="..."] ... [/tab] [/tabgroup]`

### `team_member`

- nguồn chính: harvested export
- syntax:
  - `[team_member img="..." name="..." title="..." ...][/team_member]`

### `ux_portfolio`

- nguồn chính: harvested export
- syntax:
  - `[ux_portfolio number="4" type="row" columns="2" image_height="75%"]`

## Surface vẫn pending

- `hotspot`
- `flip book`
- `message box`

Lý do:

- official demo xác nhận surface tồn tại
- nhưng chưa có shortcode thật trong harvested exports hiện có
- chưa có official doc content đủ rõ trong đợt capture này
- runtime extraction bằng browser thật đã được thử nhưng không hoàn tất được trong môi trường hiện tại

## Surface bị hạ đúng bản chất thành pattern

### `price table`

- kết luận hiện tại:
  - chưa có bằng chứng shortcode riêng trong harvested exports
  - official demo cho thấy đây có thể được dựng bằng native composition
- native composition stack thường gặp:
  - `tabgroup`
  - `row`
  - `row_inner`
  - `featured_box`
  - `divider`
  - `button`
  - list HTML nội dung

## File đã cập nhật

- `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/03-Content and Media.md`
- `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/04-Commerce and Dynamic.md`
- `VPS/docs/superpowers/flatsome-native/07-reports/Official Demo Surface Ingestion Report.md`

## Kết luận vận hành

Sau bước này, knowledge hub đã phân biệt rõ:

- cái gì là `surface official`
- cái gì là `syntax-complete`
- cái gì chỉ nên xem là `native pattern`

Điều này giúp tránh 2 lỗi lớn:

- tưởng một demo đẹp đồng nghĩa có shortcode riêng
- dạy sai syntax cho worker hoặc OpenClaw
