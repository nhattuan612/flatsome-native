# Spacing System

Date: 2026-04-24

## Mục Đích

Tài liệu này chuẩn hóa cách quyết định `spacing` cho mọi trang build bằng `Flatsome Native Builder`.

Mục tiêu:

- section có nhịp
- nội dung có khoảng thở
- không vỡ mobile
- không lạm dụng margin âm
- không sinh ra layout ngẫu nhiên khó bảo trì

## Nguồn Học Gốc

- Atlassian Spacing:
  - `https://atlassian.design/foundations/spacing/`
- IBM Carbon 2x Grid:
  - `https://carbondesignsystem.com/elements/2x-grid/overview/`
- lớp tham chiếu nội bộ từ `Flatsome Studio`

## Luật Cốt Lõi

1. Spacing là `hệ token`, không phải các con số rời rạc.
2. Mỗi trang phải có `spacing profile` trước khi build.
3. Cùng một trang không được nhảy nhịp spacing vô tổ chức.
4. Ưu tiên `section padding`, `row setting`, `col setting` trước khi thêm `gap`.
5. Margin âm chỉ dùng khi có lý do bố cục rõ ràng và phải kiểm mobile kỹ.

## Spacing Profile Phải Chốt

Mỗi `Page Plan` phải chốt:

- `Mật độ tổng thể`
  - thoáng
  - cân bằng
  - dày có chủ đích
- `Section rhythm`
- `Card padding`
- `Content stack gap`
- `CTA spacing`
- `Mobile reduction`

## Token Gợi Ý An Toàn

Hệ token gợi ý để AI suy nghĩ nhất quán:

- `2xs = 8`
- `xs = 12`
- `sm = 16`
- `md = 24`
- `lg = 32`
- `xl = 48`
- `2xl = 64`
- `3xl = 96`
- `4xl = 128`

Không bắt buộc dùng cứng từng số, nhưng phải bám một `scale` rõ ràng.

## Nhịp Spacing Theo Cấp

### Section spacing

Mặc định an toàn:

- desktop:
  - `64 - 120`
- tablet:
  - giảm một bậc
- mobile:
  - `32 - 56`

### Row / content spacing

- giữ đều giữa các block đồng cấp
- section dày nội dung có thể giảm xuống một bậc
- section kể chuyện hoặc premium có thể tăng lên một bậc

### Card padding

- card nhỏ:
  - `16 - 24`
- card nội dung chính:
  - `24 - 32`
- card premium / spotlight:
  - `32 - 48`

### Button group / CTA spacing

- giữ nút gần logic hành động
- không để CTA dính sát đoạn text
- không để CTA trôi quá xa khỏi vùng thuyết phục

## Luật Nhịp Dày Và Thưa

### 1. Không phải section nào cũng thở như nhau

Nhịp tốt cần xen kẽ:

- section hero thường thoáng hơn
- section proof/card có thể dày hơn
- CTA cuối nên gọn và rõ hơn section thông tin

### 2. Khoảng trắng phải có chủ đích

Khoảng trắng tốt là khoảng trắng:

- tách nhóm nội dung
- tạo nhịp quét mắt
- làm nổi CTA
- nâng cảm giác premium hoặc sạch

Khoảng trắng xấu là khoảng trắng:

- xuất hiện vì thiếu kiểm soát
- làm người xem tưởng trang bị lỗi
- khiến mối liên hệ nội dung bị đứt

## Dịch Sang Flatsome Native

Spacing phải được giải bằng:

- `section padding`
- `row padding`
- `col padding`
- `margin`
- `gap`
- `divider`
- `row_inner / col_inner`

Thứ tự ưu tiên:

1. `section padding`
2. `row / col setting`
3. `gap`
4. `divider` nếu cần tách nhịp rõ
5. `CSS` chỉ khi native không đủ

## Luật Không Được Làm

- không chèn quá nhiều `gap` nhỏ liên tiếp để vá layout
- không dùng margin âm như thói quen mặc định
- không để mọi section cùng một khoảng cách vô hồn
- không để text full-width quá dài vì thiếu container control
- không để touch target quá sít nhau trên mobile

## Guardrails Quan Trọng

- các nút hoặc tap target gần nhau nên có khoảng thở đủ rõ
- ảnh phải có vùng chứa ổn định, tránh content jumping
- không tạo stacking phức tạp làm nội dung bị cắt bởi `overflow hidden`
- mobile không dùng full-height thiếu kiểm soát chỉ vì muốn “đẹp”

## Checklist Nhanh Trước Khi Build

- đã chốt `spacing profile`
- đã chốt section nào thoáng, section nào dày
- đã biết hero cần nhịp nào
- đã biết card padding dùng thang nào
- đã biết mobile sẽ giảm spacing ra sao

## Checklist Audit Spacing

- section có nhịp chuyển rõ không
- có section nào bị trống vô nghĩa không
- có section nào bị nén quá chặt không
- row và col có đang đỡ nhau đúng không
- CTA có đủ khoảng thở không
- card có padding đều và đúng cấp không
- mobile có còn sạch không
- negative margin có thật sự cần không

## Kết Luận

Spacing trong hệ này là:

- `system-first`
- `rhythm-first`
- `responsive-first`
- `native-first`

Không được xem spacing chỉ là chuyện `thêm gap cho đẹp`.
