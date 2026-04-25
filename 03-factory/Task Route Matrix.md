# Task Route Matrix

Date: 2026-04-25

## Mục Đích

Đây là ma trận chọn đường build ngay sau `Input Contract`.

Nó trả lời:

- brief này là `clone`, `reinterpret`, hay `original`
- có cần mở `08-design-intelligence/` hay không
- có cần hỏi thêm hay đã đủ để sang `Page Plan`

## Luật Route

- route theo `loại input + output expectation + style source`
- không route chỉ theo `loại trang`
- nếu input mâu thuẫn, ưu tiên `output expectation`
- nếu output expectation chưa có, chưa được route

## Bảng Route Chính

| Loại input | Dấu hiệu chính | Route chuẩn | Style source mặc định | Có cần hỏi thêm không |
|---|---|---|---|---|
| `text thường` | brief mô tả bằng lời | `interpret` hoặc `creative-default` | `Flatsome Native Core` | `có`, nếu chưa rõ mức độ giống |
| `ảnh` | có screenshot/mockup/web capture | `clone` hoặc `reinterpret` | `tham chiếu ngoài` | `có`, nếu chưa rõ bám sát hay lấy tinh thần |
| `markdown spec` | có section map/logic rõ | `rebuild` | theo spec, fallback về `Flatsome Native Core` | `ít`, nếu spec đã đủ |
| `link tham chiếu` | có website/page mẫu | `clone` hoặc `reinterpret` | `tham chiếu ngoài` | `có`, nếu chưa rõ authority |
| `mixed` | text + ảnh + link + style repo | theo `output expectation` | theo nguồn được chốt | `có`, nếu các nguồn xung đột |

## Cách Chốt Mode

### `clone`

Dùng khi:

- user muốn gần giống
- reference là `primary`
- output phải giữ structure và hierarchy gần mẫu

Không được:

- tự đổi DNA lớn
- tự chuyển sang original concept

### `reinterpret`

Dùng khi:

- user muốn bám tinh thần
- reference là `secondary`
- được phép đổi section order, hero family, proof pattern

### `original`

Dùng khi:

- user chỉ đưa mục tiêu/tone
- không có reference bắt buộc
- được phép dùng `Flatsome Native Core`
- có thể mở `08-design-intelligence` nếu user muốn sáng tạo mạnh

## Khi Nào Mở Design Intelligence

Mở `08-design-intelligence/` nếu:

- user nói `sáng tạo mạnh`
- user muốn `ngôn ngữ thiết kế hiện đại`
- user đưa repo/style system/brand guideline ngoài Flatsome
- task thuộc `creative-modern`
- task là `reinterpret` nhưng cần nâng cấp visual language rõ rệt

Không mở nếu:

- user chỉ muốn build theo mặc định Flatsome
- task là clone sát mẫu

## Khi Nào Dùng Flatsome Native Core

Dùng mặc định nếu:

- brief ngắn
- không có reference ngoài
- user không yêu cầu style system riêng
- task chỉ cần `đẹp, rõ, native, editable`

## Trích Xuất Từ Ảnh / Link

Nếu input là `ảnh` hoặc `link`, worker phải trích ra tối thiểu:

- layout tổng
- hierarchy nội dung
- hero type
- rhythm spacing
- card density
- CTA pattern
- proof pattern
- typography mood
- màu chính/phụ
- motion cảm nhận được nếu có

Nếu chưa trích được các mục này:

- chưa được route là `clone`

## Tình Huống Mẫu Tự Kiểm

### Case 1

- Input:
  - brief text ngắn
  - không có ảnh
  - muốn theo Flatsome mặc định
- Route:
  - `creative-default`
- Style source:
  - `Flatsome Native Core`
- Output expectation:
  - `original`
- Có cần hỏi thêm:
  - `có`, nếu thiếu CTA hoặc thiết bị ưu tiên

### Case 2

- Input:
  - brief text ngắn
  - muốn sáng tạo mạnh
- Route:
  - `creative-modern`
- Style source:
  - `Flatsome Native Core + Design Intelligence`
- Output expectation:
  - `original`

### Case 3

- Input:
  - ảnh chụp landing page
  - yêu cầu clone bằng UX Builder editable
- Route:
  - `clone`
- Style source:
  - `tham chiếu ngoài`
- Output expectation:
  - `clone`

### Case 4

- Input:
  - markdown spec đầy đủ section map
- Route:
  - `rebuild`
- Style source:
  - `theo spec`
- Output expectation:
  - `reinterpret` hoặc `original` tùy spec đã khóa

### Case 5

- Input:
  - link tham chiếu
  - yêu cầu `bám tinh thần, không clone`
- Route:
  - `interpret`
- Style source:
  - `tham chiếu ngoài`
- Output expectation:
  - `reinterpret`

### Case 6

- Input:
  - text + ảnh + repo style tham khảo
- Route:
  - theo `output expectation` đã chốt
- Style source:
  - `tham chiếu ngoài` hoặc `Flatsome Native Core + Design Intelligence`
- Output expectation:
  - phải khóa trước khi build

## Kết Luận

Worker muốn route đúng thì dùng file này ngay sau `Input Contract`, trước `Page Goal Routing.md`.
