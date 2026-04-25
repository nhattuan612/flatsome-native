# Báo Cáo Bổ Sung Lớp Typography Và Spacing

Date: 2026-04-24

## Mục Tiêu

Đưa `Typography` và `Spacing` thành 2 lớp tri thức riêng trong kho `Flatsome Native Builder`, để AI và operator không chỉ build theo layout mà còn kiểm soát tốt hơn:

- hierarchy chữ
- readability
- spacing rhythm
- responsive spacing

## Đã Tạo

- `03-factory/Typography System.md`
- `03-factory/Spacing System.md`

## Đã Cập Nhật

- `01-platform/Operating Law.md`
- `03-factory/Design Language Reference.md`
- `03-factory/Factory Overview.md`
- `03-factory/README.md`
- `05-flows/UI Build Script.md`
- `05-flows/Final QA Checklist.md`
- `06-templates/Page Plan Template.md`
- `START HERE.md`
- `README.md`

## Kết Luận Học Được

1. Typography phải được xem như `role system`, không phải chỉ là chọn font.
2. Spacing phải được xem như `token + rhythm system`, không phải margin rời rạc.
3. `Page Plan` bắt buộc phải chốt typography và spacing profile trước khi build.
4. `QA` phải kiểm typography/spacing như điều kiện pass, không chỉ nhìn chung chung.
5. Hai lớp này phải đứng ở `03-factory` vì đây là lớp dịch tri thức thiết kế sang quyết định build thực tế.

## Nguồn Học Gốc

- Atlassian Design System
- IBM Carbon Design System
- W3C WCAG Text Spacing
- quan sát ngược từ các surface mạnh của Flatsome

## Ảnh Hưởng Vận Hành

Từ mốc này, AI muốn build tốt phải đọc thêm:

- `03-factory/Typography System.md`
- `03-factory/Spacing System.md`

trước khi chốt `Page Plan`.
