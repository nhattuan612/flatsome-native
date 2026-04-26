# Factory Pattern Upgrade Report

Date: 2026-04-24

## Trạng thái

`PASS: factory upgraded from syntax-confirmed surfaces`

## Mục tiêu

Biến phần `language map` đã xác minh thành:

- archetype dùng lại được
- page skeleton rõ hơn
- rule tách block thực dụng hơn

## Archetype mới đã thêm

- `Contact split with map`
- `Team roster grid`
- `Portfolio showcase rail`
- `Tabbed FAQ / pricing panel`
- `Testimonial + logo proof rail`
- `Video trigger banner`
- `Instagram / social proof strip`

## Skeleton mới đã thêm

- `Contact page`
- `Portfolio / case-study landing`
- `Service / agency page`
- `Pricing / FAQ page`

## Nâng cấp Block Registry

Đã thêm:

- danh sách block thư viện nên ưu tiên tách
- công thức đặt tên block theo `loại + mood/layout + mục đích`
- dấu hiệu nên tách block ngay khi archetype đã ổn định

## Giá trị vận hành

Sau nâng cấp này:

- worker chọn section nhanh hơn từ page goal
- giảm việc dựng lại section quen thuộc từ số 0
- tăng cơ hội tái dùng block đúng chuẩn công ty
- giữ được native structure rõ và editability trong UX Builder

## File đã cập nhật

- `03-factory/Section Archetypes.md`
- `03-factory/Composition Rules.md`
- `03-factory/Block Registry.md`
- `07-reports/Factory Pattern Upgrade Report.md`
