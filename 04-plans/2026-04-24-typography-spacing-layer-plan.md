# Typography Và Spacing Layer Plan

Date: 2026-04-24

## Mục Tiêu

Bổ sung lớp tri thức `Typography` và `Spacing` vào bộ não `Flatsome Native Builder` theo hướng:

- ngắn gọn
- đọc nhanh
- áp dụng được ngay vào `Page Plan`
- kiểm được ở `QA`
- không làm phình kho tri thức vô ích

## Phạm Vi

### Tạo mới

- `03-factory/Typography System.md`
- `03-factory/Spacing System.md`
- `07-reports/Typography and Spacing Layer Report.md`

### Cập nhật

- `01-platform/Operating Law.md`
- `03-factory/Design Language Reference.md`
- `03-factory/Factory Overview.md`
- `03-factory/README.md`
- `05-flows/UI Build Script.md`
- `05-flows/Final QA Checklist.md`
- `06-templates/Page Plan Template.md`
- `START HERE.md`
- `README.md`

## Kết Quả Mong Muốn

1. AI biết `Typography` và `Spacing` là lớp quyết định bắt buộc trước khi build.
2. `Page Plan` có chỗ ghi rõ hướng chữ và nhịp spacing.
3. `QA` có tiêu chí kiểm typography/spacing cụ thể hơn.
4. Người đọc mới có đường vào ngắn, không phải mò.
5. Toàn bộ vẫn bám `section-first`, `native-first`, `>=90% native`.

## Nguồn Học Gốc

- Atlassian Design System
- IBM Carbon Design System
- W3C WCAG Text Spacing
- lớp tham chiếu nội bộ từ `Flatsome Studio`

## Ghi Chú Triển Khai

- không gắn với một brand cụ thể
- không áp một font cố định cho toàn hệ
- ưu tiên `type roles`, `spacing tokens`, `translation to Flatsome`
- không thêm file nếu chỉ là lặp nội dung cũ
