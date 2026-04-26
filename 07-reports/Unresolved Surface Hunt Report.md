# Unresolved Surface Hunt Report

Date: 2026-04-24

## Trạng thái

`PASS: unresolved surfaces were classified honestly`

## Phạm vi

Đợt này chỉ săn 3 surface khó:

- `hotspot`
- `flip book`
- `message box`

## Nguồn đã dùng

### Official demo pages

- https://demos.flatsome.com/elements/hotspot/
- https://demos.flatsome.com/elements/flip-book/
- https://demos.flatsome.com/elements/message-box/

### Harvested data

- `data/flatsome-studio/exports (ngoài hub)/*.json`
- `data/ (ngoài hub) flatsome-studio/catalog.ndjson`
- `data/ (ngoài hub) flatsome-studio/slot-map.ndjson`

### Runtime attempt

- thử Chrome + CDP local để trích runtime/DOM thật
- không hoàn tất được trong môi trường hiện tại

## Kết quả

### `hotspot`

- official demo: xác nhận là surface có thật
- official value:
  - dùng cho storytelling trên ảnh
  - đi tốt với `banner + hotspot + slider`
- harvested exports:
  - chưa thấy shortcode thật
- kết luận:
  - `official surface`
  - `pattern-level value` rất cao
  - `syntax unresolved`

### `flip book`

- official demo: xác nhận surface tồn tại
- official value:
  - dùng cho trình bày kiểu flip/reveal
  - có giá trị với product teaser và card-like presentation
- harvested exports:
  - chưa thấy shortcode thật
- kết luận:
  - `official presentational surface`
  - `syntax unresolved`

### `message box`

- official demo: xác nhận use case CTA/callout/notice
- harvested exports:
  - chưa thấy shortcode thật
- kết luận:
  - `official CTA/callout surface`
  - có thể là builder surface hiếm hoặc serialize theo cách khác
  - `syntax unresolved`

## Quy tắc vận hành sau đợt này

Đối với 3 surface trên:

- không tự bịa shortcode
- không dạy worker syntax giả
- chỉ dùng như `surface/pattern knowledge`
- khi nào capture được shortcode thật hoặc doc chính thức rõ hơn thì mới nâng lên `syntax-complete`

## File đã cập nhật

- `01-platform/native-builder-language/03-Content and Media.md`
- `07-reports/Official Surface Syntax Capture Report.md`
- `07-reports/Unresolved Surface Hunt Report.md`

## Kết luận

Đợt săn này không làm knowledge hub “đầy hơn” theo số lượng syntax, nhưng làm nó đúng hơn.

Đó là lợi ích lớn hơn:

- giữ tính toàn vẹn
- giữ tính nhất quán
- tránh học sai Builder language
