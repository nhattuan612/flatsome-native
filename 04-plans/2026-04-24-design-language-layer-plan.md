# Kế Hoạch Bổ Sung Lớp Design Language

Date: 2026-04-24

## Mục Tiêu

Bổ sung một lớp tri thức mới để:

- tăng độ chuyên nghiệp của UI
- chống lặp bố cục
- cho phép tham chiếu các design system hiện đại
- nhưng vẫn giữ `Flatsome Native Core` là mặc định

## Phạm Vi

Tạo và nối các file sau:

- `03-factory/Design Language Reference.md`
- `03-factory/Layout DNA.md`
- `03-factory/No Repeat Law.md`
- `03-factory/Section Order Recipes.md`

Và cập nhật các file điều hướng / vận hành liên quan.

## Luật Thiết Kế

- external design systems chỉ là `tham khảo`
- Native Core từ `111 Full Page` vẫn là gốc
- không biến repo ngoài thành luật mặc định
- mọi thứ vẫn phải dịch về `section-first`

## Kết Quả Mong Muốn

Sau khi hoàn tất:

- AI đọc hub biết cách làm trang chuyên nghiệp hơn
- AI mặc định tránh lặp bố cục trang trước
- Page Plan có chỗ ghi `Layout DNA`, `recipe`, và `nguồn tham khảo`
- luồng build chính nhận biết rõ lớp design-language mới
