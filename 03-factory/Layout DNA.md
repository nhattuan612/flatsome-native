# Layout DNA

Date: 2026-04-24

## Mục Đích

Tài liệu này định nghĩa `DNA bố cục` của một trang trước khi build.

Nếu `Page Plan` không chốt `Layout DNA`, khả năng cao trang sẽ:

- rơi về một bố cục an toàn lặp lại
- giống trang trước quá nhiều
- thiếu cá tính

## Layout DNA Là Gì

`Layout DNA` là bộ quyết định cấp cao trả lời:

- trang này kể chuyện theo nhịp nào
- hero kiểu gì
- section nặng hình hay nặng nội dung
- CTA xuất hiện ở đâu
- giao diện thiên phẳng, card, editorial hay showroom

## Các Trục Phải Chốt

Mỗi trang phải chốt ít nhất các trục sau:

### 1. Hero Family

Chọn một trong các họ chính:

- `statement hero`
- `slider hero`
- `split hero`
- `offset card hero`
- `media wall hero`
- `product focus hero`
- `editorial hero`

### 2. Section Rhythm

Chọn một nhịp chính:

- `đều và sạch`
- `xen kẽ đậm nhạt`
- `dồn cao trào về cuối`
- `mở mạnh rồi thả lỏng`
- `nén đầu trang, giãn cuối trang`

### 3. Dominant Geometry

Chọn hình học chủ đạo:

- `full width banner`
- `grid card`
- `split 50/50`
- `staggered collage`
- `stacked content bands`
- `asymmetric offset`

### 4. Content Density

Chọn mật độ:

- `thoáng`
- `trung bình`
- `dày thông tin`

### 5. Visual Weight

Chọn thứ nặng nhất:

- `headline`
- `ảnh`
- `card`
- `proof`
- `CTA`

### 6. CTA Pattern

Chọn mô hình CTA:

- `1 CTA mạnh ở hero`
- `hero + mid CTA + close CTA`
- `CTA mềm dạng khám phá`
- `CTA dày kiểu bán hàng`

### 7. Motion Profile

Chọn profile chuyển động:

- `tối giản`
- `êm`
- `rõ vừa`
- `giàu motion nhưng kiểm soát`

### 8. Proof Pattern

Chọn dạng chứng minh:

- `testimonial band`
- `logo rail`
- `stat counters`
- `case cards`
- `team trust`

## Công Thức Chốt DNA

Trước khi viết shortcode, phải ghi được dòng sau:

`Hero Family + Section Rhythm + Dominant Geometry + Content Density + CTA Pattern + Motion Profile`

Ví dụ:

- `offset card hero + xen kẽ đậm nhạt + asymmetric offset + thoáng + hero-mid-close CTA + êm`
- `media wall hero + mở mạnh rồi thả lỏng + staggered collage + trung bình + CTA mềm + rõ vừa`

## Luật CEO

1. Cùng một brief mà `Layout DNA` giống hệt trang trước thì xem như chưa sáng tạo đủ.
2. Không được chỉ đổi màu rồi giữ nguyên DNA cũ.
3. Nếu brand cần đồng bộ, chỉ giữ:
   - font
   - tone màu
   - mức độ sang trọng / trẻ trung
4. Còn `hero family`, `section rhythm`, `geometry`, `CTA pattern` phải ưu tiên thay đổi khi không có lệnh giữ nguyên.

## Mối Liên Hệ Với Page Plan

`Page Plan` bắt buộc phải có:

- `Layout DNA đã chọn`
- `Lý do chọn DNA`
- `DNA có trùng trang gần nhất không`

Nếu trùng:

- phải ghi lý do
- hoặc đổi recipe

## Mapping Nhanh Sang Native Elements

### Statement hero

- `section`
- `row`
- `title`
- `text`
- `button`
- `banner` nếu cần nền media

### Slider hero

- `ux_slider`
- `ux_banner`
- `text_box`
- `button`

### Offset card hero

- `banner`
- `row`
- `col`
- `text`
- `button`
- margin / padding native

### Media wall hero

- `row_inner`
- `col_inner`
- `image`
- `banner`
- `gallery`

### Grid-card heavy page

- `featured_box`
- `image_box`
- `icon_box`
- `row_inner`

### Editorial page

- `title`
- `text`
- `blog_posts`
- `banner`
- `divider`

## Kết Luận

`Layout DNA` là lớp chống build theo quán tính.

Không chốt DNA thì không được xem là đã lên plan đủ sâu.
