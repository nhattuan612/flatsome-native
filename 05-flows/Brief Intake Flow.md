# Brief Intake Flow

Date: 2026-04-24

## Mục Đích

Đây là flow chuẩn hóa brief trước `Page Plan`.

Nó tồn tại để chặn các lỗi phổ biến:

- nhảy vào build khi brief còn mơ hồ
- chọn sai `Page Type`
- nhầm `mục tiêu chính`
- thiếu CTA, tone, motion, thiết bị ưu tiên
- build ra trang đẹp nhưng không đúng mục tiêu
- nhầm `clone` thành `creative`
- nhầm `reference chính` thành `chỉ để tham khảo`

## Chuỗi Bắt Buộc

`Input Contract -> Brief chuẩn hóa V2 -> Route -> Page Plan -> Build`

Không được bỏ qua bước `Input Contract`.
Không được bỏ qua bước `Brief chuẩn hóa`.

Nếu brief có dấu hiệu yêu cầu sáng tạo hoặc cần đề xuất thiết kế:

- mở `08-design-intelligence/Design Mode Router.md`
- chốt `Design Mode` trước khi sang `Page Plan`

Nếu brief có ảnh, link hoặc mixed input:

- mở `03-factory/Task Route Matrix.md`
- không route chỉ bằng cảm tính

## Đầu Vào Tối Thiểu Phải Có

- `Loại input`
- `Loại trang`
- `Mục tiêu trang`
- `Output expectation`
- `CTA chính`
- `Tone giao diện`
- `Thiết bị ưu tiên`

Nếu thiếu:

- ghi `không xác định`
- dùng `default an toàn`
- không được tự bịa

## Default An Toàn

- `Tone giao diện:`
  - sáng
  - sạch
  - hiện đại
- `Thiết bị ưu tiên:`
  - mobile trước
- `Motion:`
  - nhẹ
  - không gây nhiễu
- `CTA chính:`
  - 1 CTA rõ
- `Cấu trúc:`
  - section tách rõ
  - row rõ
  - không nhồi quá nhiều element vào một vùng

## Bước 1: Chuẩn Hóa Brief

Mở:

- `05-flows/Input Contract.md`

Phải chốt được các trường sau:

- `Loại input`
- `Input gốc`
- `Tên trang`
- `Loại trang`
- `Mục tiêu trang`
- `Mục tiêu task`
- `Output expectation`
- `Mức độ sáng tạo`
- `Style source`
- `Reference authority`
- `CTA chính`
- `Tone giao diện`
- `Màu chủ đạo`
- `Font mong muốn`
- `Phong cách motion`
- `Design Mode`
- `Style family`
- `Pattern family`
- `Typography mood`
- `Spacing rhythm`
- `Motion profile`
- `Anti-patterns cần tránh`
- `Thiết bị ưu tiên`
- `Mức độ giống mẫu tham chiếu`
- `Ràng buộc thương hiệu`
- `Unknowns`
- `Default an toàn`

Nếu là input `ảnh / link / mixed`, phải trích thêm:

- `layout tổng`
- `hierarchy`
- `hero type`
- `spacing rhythm`
- `CTA pattern`
- `proof pattern`

Nếu chưa trích được, chưa được khóa route clone.

## Bước 2: Route

Mở:

- `03-factory/Task Route Matrix.md`
- `03-factory/Page Goal Routing.md`

Phải chốt:

- `Route label`
- `Output expectation`
- `Style source`
- `Reference authority`
- `Skeleton`
- `Archetype ưu tiên`
- `Ứng viên block nên tái dùng`
- `Ứng viên block nên tạo mới`
- `Design Mode`
- `Style family`
- `Pattern family`
- `Typography mood`
- `Spacing rhythm`
- `Motion profile`
- `Anti-patterns cần tránh`

## Bước 3: Nối Với Starter Snippets

Mở:

- `03-factory/Section Starter Snippets.md`

Chỉ chọn snippet nếu:

- đúng `Skeleton`
- đúng `Archetype`
- không ép sai mục tiêu

## Bước 4: Bàn Giao Sang Page Plan

Mở:

- `06-templates/Page Plan Template.md`

Phải điền đủ:

- `Input Contract`
- `Build Readiness`
- `Section Count`
- `Tổng số row dự kiến`
- `Tổng số col chính dự kiến`
- `Section Map`
- `Reuse từ block sẵn có`
- `Risk Notes`

## Gói Đầu Ra Chuẩn

Trước khi build, worker phải có đúng gói đầu ra này:

- `Brief chuẩn hóa V2`
- `Output expectation`
- `Style source`
- `Reference authority`
- `Unknowns`
- `Default an toàn`
- `Route label`
- `Skeleton đã chọn`
- `Archetype ưu tiên`
- `Ứng viên block`
- `Page Plan`
- `Section Map`

## Mẫu Brief Nén 1 Dòng

```txt
Loại input | Loại trang | Mục tiêu | Output expectation | CTA chính | Tone | Thiết bị ưu tiên | Style source | Skeleton
```

## Mẫu Brief Chuẩn Hóa Ngắn

```txt
Loại input:
Input gốc:
Tên trang:
Loại trang:
Mục tiêu trang:
Mục tiêu task:
Output expectation:
Mức độ sáng tạo:
Style source:
Reference authority:
CTA chính:
Tone giao diện:
Màu chủ đạo:
Font mong muốn:
Phong cách motion:
Design Mode:
Style family:
Pattern family:
Typography mood:
Spacing rhythm:
Motion profile:
Anti-patterns cần tránh:
Thiết bị ưu tiên:
Mức độ giống mẫu tham chiếu:
Ràng buộc thương hiệu:
Unknowns:
Default an toàn:
Route label:
Skeleton đã chọn:
Archetype ưu tiên:
Ứng viên block nên tái dùng:
Ứng viên block nên tạo mới:
```

## Luật CEO

- chưa qua `Input Contract` thì chưa được build
- brief chưa route được thì chưa được build
- chưa chốt `output expectation` thì chưa được build
- chưa chốt `style source` thì chưa được build
- chưa chốt CTA chính thì chưa được build
- chưa có `Section Map` thì chưa được build
- thiếu dữ liệu thì ghi `không xác định`, không được tự bịa
