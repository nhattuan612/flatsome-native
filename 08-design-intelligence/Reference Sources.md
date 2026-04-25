# Reference Sources

Date: 2026-04-24

## Mục Đích

Tài liệu này quy định cách hấp thụ tri thức từ nguồn ngoài một cách `khéo`, `an toàn`, và `không biến thành ăn cắp`.

## Nguồn Gốc Của Lớp Này

Hai nguồn gợi ý chính cho lớp `Design Intelligence`:

- `Global Design System Index`
  - dùng như một `index` lớn trỏ tới design systems khác
  - repo có `Unlicense`
  - nhưng từng hệ thiết kế được link tới có license riêng, phải tự kiểm khi dùng sâu
- `Advanced UI/UX Logic Framework`
  - dùng như một ví dụ tốt về:
    - reasoning engine
    - pattern + style + colors + typography + effects
    - anti-pattern thinking
    - `MASTER + page override`
  - repo có `MIT`

## Chỉ Được Hấp Thụ Cái Gì

### Được hấp thụ

- cách phân loại style
- cách route product -> style -> pattern
- cách tách:
  - typography
  - spacing
  - motion
  - anti-pattern
- cách tổ chức `MASTER` và `page override`
- cách trình bày recommendation ngắn gọn, dễ dùng

### Không được hấp thụ thô

- nguyên văn mô tả dài của repo khác
- assets
- screenshots
- icon set riêng
- token màu của brand khác như một default mặc định
- component code của hệ khác
- wording đặc trưng của một brand

## Quy Tắc “Chôm Khéo”

1. Chôm `khung suy nghĩ`, không chôm `nội dung thô`.
2. Đọc `official docs` trước khi tin một chỉ mục tổng hợp.
3. Tự viết lại bằng ngôn ngữ và luật của công ty.
4. Luôn dịch qua bộ lọc:
   - `section-first`
   - `native-first`
   - `editable in UX Builder`
5. Nếu một ý tưởng ngoài không dịch nổi về native builder, hạ ưu tiên.

## Vai Trò Của Mỗi Nguồn

### `Global Design System Index`

Dùng để:

- mở rộng phạm vi tham khảo
- tìm official docs nhanh hơn
- gợi ý cho user các hướng design language

Không dùng để:

- làm rule mặc định
- copy style trực tiếp

### `Advanced UI/UX Logic Framework`

Dùng để học:

- kiến trúc dữ liệu UI
- flow recommendation
- anti-pattern layer
- cấu trúc `MASTER + override`

Không dùng để:

- copy database của họ
- copy prompt / search engine / scripts

## Kết Luận

Nguồn ngoài là:

- `bàn đạp tư duy`
- `bản đồ tham khảo`

không phải `bộ não mặc định`.
