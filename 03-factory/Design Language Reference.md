# Design Language Reference

Date: 2026-04-24

## Mục Đích

Tài liệu này là lớp `tham khảo và dịch ngôn ngữ thiết kế` cho hệ `Flatsome Native Builder`.

Mục tiêu:

- giữ gốc `section-first`
- giữ output `shortcode-native`
- giữ khả năng mở lại bằng `UX Builder`
- tăng độ chuyên nghiệp của UI
- cho phép tiếp thu nhiều ngôn ngữ thiết kế hiện đại mà không đánh mất DNA gốc của hệ Flatsome

Tài liệu này `không` phải là luật cao nhất.

## Thứ Tự Ưu Tiên

Khi có xung đột, áp dụng đúng thứ tự sau:

1. `01-platform/Operating Law.md`
2. brief và brand rule đã chốt với người giao việc
3. `111 Full Page` của `Flatsome Studio` và các bề mặt native đã xác minh
4. `03-factory/Design Language Reference.md`
5. repo hay nguồn tham khảo bên ngoài

Kết luận:

- nguồn ngoài chỉ là `tham khảo`
- không được ép thành mặc định
- không được phá `native >= 90%`

## Native Design Core Của Công Ty

Hệ ngôn ngữ thiết kế gốc của công ty phải sinh ra từ:

- `111 Full Page` trong `Flatsome Studio`
- catalog `492-slot`
- các surface official demo đã hút
- các archetype và recipe đã chuẩn hóa trong `03-factory/`

Điều này bảo đảm:

- build được bằng chính ngôn ngữ của Flatsome
- mở lại kéo thả được
- không lệ thuộc vào một brand hay một website cụ thể

## Vai Trò Của Design Language Ở Lớp Factory

Ở lớp `03-factory`, file này dùng để:

- dịch một design language thành quyết định build
- nối design direction sang `Layout DNA`
- nối design direction sang `Section Order Recipe`
- giữ output cuối vẫn là `Flatsome Native`

Nếu cần rule về:

- nguồn tham khảo ngoài
- cách hấp thụ repo ngoài
- source usage rule

thì source of truth nằm ở:

- `08-design-intelligence/README.md`
- `08-design-intelligence/Design Mode Router.md`
- `08-design-intelligence/Reference Sources.md`

File này không còn giữ ownership cho source usage rule.

Những ý tưởng ngoài `không` được dùng để:

- áp đặt layout không native vào Flatsome
- biến `ux_html` thành khung chính
- copy nguyên xi một hệ thiết kế mà không dịch sang cấu trúc `section -> row -> col -> element`

## Nguồn Tham Khảo

Danh sách nguồn tham khảo và source usage rule đã được tách sang:

- `08-design-intelligence/Reference Sources.md`

## Học Gì Từ Một Design Language

Khi phân tích một ngôn ngữ thiết kế, phải bóc tách tối thiểu các lớp sau:

### 1. Nhịp bố cục

- section dài hay ngắn
- nhiều khoảng thở hay dày nội dung
- nhịp xen kẽ sáng tối ra sao
- section chuyển tiếp mềm hay dứt khoát

### 2. Hệ phân cấp chữ

- headline lớn tới mức nào
- subheadline dài hay ngắn
- body copy cô đọng hay giải thích sâu
- CTA có tách cấp rõ không
- type roles nào là bắt buộc
- text width có bị quá dài không

### 2b. Hệ typography

- font mang tính cách gì
- heading và body tách vai trò ra sao
- line-height dày hay thoáng
- mobile có còn đọc được không

### 2c. Hệ spacing

- section spacing rộng hay nén
- card padding dày hay gọn
- CTA có khoảng thở không
- nhịp spacing có đều theo token hay ngẫu nhiên

### 3. Hình học giao diện

- bo góc mạnh hay ít
- card phẳng hay có depth
- ảnh full-bleed hay nằm trong khung
- grid cứng hay lệch nhịp có chủ đích

### 4. Màu và độ tương phản

- nền sáng hay tối
- màu nhấn dùng để làm gì
- CTA dùng màu nổi hay nền trung tính
- độ tương phản có đủ để đọc và bấm không

### 5. Ảnh và media

- ảnh thiên về lifestyle hay sản phẩm
- crop gần hay xa
- có dùng video, slider, gallery, hotspot không
- ảnh đóng vai trò hero hay chỉ bổ trợ

### 6. Motion

- animate nhẹ hay rõ
- section xuất hiện theo nhịp nào
- hover có sắc hay mềm
- motion có phục vụ CTA hay chỉ để trang trí

### 7. Mô hình CTA

- CTA nằm ở hero, giữa trang, cuối trang hay cả ba
- CTA mang tính bán hàng, khám phá hay dẫn đọc
- CTA nổi bật bằng màu, vị trí hay spacing

## Cách Dịch Design Language Sang Flatsome Native

Không được bê nguyên mô tả thẩm mỹ vào build. Phải dịch theo tuyến sau:

`Design language -> Layout DNA -> Section Order Recipe -> Section Map -> Native elements -> Setting native -> CSS tối thiểu nếu bắt buộc`

### Bước dịch chuẩn

1. xác định `tính cách giao diện`
2. xác định `hero type`
3. xác định `section order`
4. xác định `mật độ nội dung`
5. xác định `typography direction`
6. xác định `spacing profile`
7. xác định `motion profile`
8. map sang `archetype` trong `03-factory`
9. chọn `native elements` tương ứng
10. chỉ sau cùng mới cân nhắc `CSS`

## Bản Dịch Nhanh Từ Một Số Hệ Thiết Kế Lớn

### Apple

- nên học:
  - hero kể chuyện bằng sản phẩm
  - khoảng thở lớn
  - headline mạnh
  - section chuyển cảnh sạch và gọn
- nên dịch sang Flatsome bằng:
  - `banner`
  - `section` lớn với spacing rộng
  - `title`
  - `text`
  - `button`
  - `slider` hoặc image bands
- không nên làm:
  - nhồi quá nhiều card nhỏ vào trang kiểu Apple

### Fluent

- nên học:
  - cảm giác mềm, gần gũi
  - lớp nền sáng, surface nổi vừa phải
  - card và icon thân thiện
- nên dịch bằng:
  - `icon_box`
  - `featured_box`
  - `message_box`
  - `row/col` với nền layer nhẹ

### Carbon

- nên học:
  - tính hệ thống
  - grid chặt
  - hierarchy rõ
  - nội dung enterprise, giàu thông tin
- nên dịch bằng:
  - `tabs`
  - `accordion`
  - `title`
  - `text`
  - `row/col` grid chặt

### Atlassian

- nên học:
  - rõ việc, rõ hành động
  - phân khu thông tin dễ quét
  - CTA điều hướng sản phẩm rất rõ
- nên dịch bằng:
  - section nhiều tầng thông tin
  - `tabs`
  - `blog_posts`
  - `button`
  - `icon_box`

### Material

- nên học:
  - state và component thinking
  - layer rõ
  - card/grid có quy luật
- nên dịch bằng:
  - `image_box`
  - `featured_box`
  - `accordion`
  - `tabs`
  - `button`

## Luật Giữ Gốc

1. Không dùng repo ngoài như luật cứng mặc định.
2. Không để một website tham chiếu đơn lẻ trở thành style gốc của công ty.
3. Mọi thiết kế đẹp đến đâu cũng phải dịch về `section-first`.
4. Nếu một ý tưởng không mở lại được bằng UX Builder thì ý tưởng đó chưa đạt.
5. Nếu một phong cách cần quá nhiều HTML để giả lập, phải hạ ưu tiên hoặc thay hướng.

## Khi Nào Phải Mở File Này

- khi brief nói `phong cách Apple`, `phong cách hiện đại`, `muốn chuyên nghiệp hơn`
- khi cần tạo biến thể mới mà không muốn lặp bố cục cũ
- khi user đưa một repo design system, một website mẫu, hoặc brand guideline
- khi muốn nâng chất lượng thẩm mỹ nhưng vẫn giữ native

## File Liên Quan Phải Đọc Cùng

- `03-factory/Typography System.md`
- `03-factory/Spacing System.md`
- `03-factory/Layout DNA.md`
- `03-factory/No Repeat Law.md`
- `03-factory/Section Order Recipes.md`
- `03-factory/Page Goal Routing.md`
- `03-factory/Section Archetypes.md`

## Kết Luận

`03-factory/Design Language Reference.md` là bộ chuyển ngữ:

- từ `ngôn ngữ thiết kế`
- sang `Flatsome Native Builder`

Nó làm trang `chuyên nghiệp hơn`, `đa dạng hơn`, nhưng vẫn `giữ gốc Flatsome`.
