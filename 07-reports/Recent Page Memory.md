# Recent Page Memory

Date: 2026-04-25

## Mục Đích

Đây là bộ nhớ vận hành ngắn hạn để novelty gate so với các trang gần nhất.

Tài liệu này `không` phải tri thức tổng quát.

Nó là:

- bộ nhớ so sánh
- nhật ký layout gần đây
- nguồn dữ liệu cho `Novelty Scoring`

## Luật Dùng

1. Chỉ cập nhật file này khi page thật sự đáng tham gia novelty gate của các task sau.
2. Trước khi build page mới phải so với ít nhất `3` dòng gần nhất liên quan.
3. Nếu không cập nhật file này, `Novelty Scoring` bị xem là thiếu dữ liệu.

## Khi Nào Không Được Cập Nhật

Không cập nhật file này nếu task là:

- `harvest-task`
- `extract-task`
- `system-doc-task`
- sửa docs / luật / flow
- sửa lỗi nhỏ không làm đổi `Layout DNA`
- sửa syntax / parser / CSS nhỏ mà không đổi bố cục trọng yếu

## Khi Nào Được Cập Nhật

Chỉ cập nhật khi:

- đây là `page-task`
- page đã qua `Release Gate`
- page là page mới hoặc rebuild đủ lớn
- novelty axes có giá trị so về sau:
  - `Hero Family`
  - `Layout Pool`
  - `Dominant Geometry`
  - `CTA Pattern`

`Rebuild đủ lớn` nên hiểu là đúng ít nhất `1` trong các trường hợp:

- đổi ít nhất `2/4` novelty axes trọng yếu:
  - `Hero Family`
  - `Layout Pool`
  - `Dominant Geometry`
  - `CTA Pattern`
- đổi `Section Order Recipe` và đổi rõ hierarchy chính của trang
- đổi hero structure + flow chuyển đổi tổng thể, làm page cần được so riêng ở task sau

Không cập nhật nếu chỉ:

- sửa copy
- thay ảnh nhưng giữ nguyên cấu trúc chính
- chỉnh font / màu / CSS nhỏ
- vá responsive / spacing / syntax
- sửa CTA wording nhưng không đổi CTA pattern

## Quy Tắc CEO

- không dùng file này như nhật ký mọi task
- chỉ ghi những page thật sự cần tham gia novelty gate của các page sau
- nếu chỉ sửa nhỏ mà vẫn cập nhật, novelty memory sẽ bị nhiễu

## Bản Ghi Gần Nhất

| Post ID | Tên trang | Loại trang | Hero Family | Layout Pool | Dominant Geometry | CTA Pattern | Ghi chú novelty |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1174 | Harborline Quiet Portfolio 2026-04-25 | landing / premium real-estate quiet-editorial test | media wall hero | Pool C: Media Wall Narrative | editorial text rail + staggered media wall + calm compare cards | hero + close | khác rõ skyline vì bỏ stats, tabs, timeline, access deck; đi theo quiet-editorial sequence và headline guardrail chặt hơn |
| 1172 | Skyline District Command Center 2026-04-25 | landing / premium real-estate command center test | split signal hero | Pool F: Command Editorial | left narrative + right mosaic + dashboard metrics + alternating bands | hero + mid + close | khác rõ với chuỗi slider cũ và cũng không lặp dark collage; dùng command-editorial logic và mid-page focus slider |
| 1154 | Lumen District Creative Native Test 2026-04-24 | homepage / creative real-estate test | split collage hero | Pool H: Editorial Collage | split collage + mosaic + proof cards | hero + narrative + close | khác rõ với toàn bộ chuỗi slider / Pool A và dùng font theme mới |
| 1150 | Asteria Stay Editorial 2026-04-24 | homepage / hospitality | offset card hero | Pool D: Offset Editorial | asymmetric offset + editorial split + staggered gallery | CTA mềm dạng khám phá | khác rất mạnh với chuỗi safe pattern |
| 1148 | Asteria Stay Narrative 2026-04-24 | homepage / hospitality | media wall hero | Pool C: Media Wall Narrative | collage + staggered image + overlay cards | CTA mềm giữa trang + close CTA rõ | khác rất mạnh với pool cũ |
| 1146 | Infant Milk Powder Fluent Native 2026-04-24 | landing / product marketing | statement hero | Pool B: Statement Soft Cards | asymmetric offset + soft cards | hero + close, mid CTA nhẹ | khác rõ với 1144 |
| 1144 | Infant Milk Powder Native Core 2026-04-24 | landing / product marketing | slider hero | Pool A: Slider Commerce | grid card + split section | hero + mid + close | còn gần safe pattern cũ |
| 1142 | Orange Juice Apple Style Native 2026-04-24 | homepage / product marketing | statement hero | Pool E: Dark Showcase | showcase + line-up + split | hero + close | khá mới ở thời điểm tạo |
| 1140 | Orange Juice Purple Home Native 2026-04-24 | homepage / product marketing | slider hero | Pool A: Slider Commerce | grid card + split section | hero + mid + close | lặp nhiều với 1136 |
| 1136 | Orange Juice Home Native 2026-04-24 | homepage / product marketing | slider hero | Pool A: Slider Commerce | grid card + split section | hero + mid + close | safe pattern rõ |
| 1134 | Real Estate Home Native 2026-04-24 | homepage | slider hero | Pool A: Slider Commerce | grid card + split section | hero + mid + close | safe pattern rõ |
| 1132 | Sales Native Test 2026-04-24 | landing / sales | statement hero | Pool G: Proof-First | band + proof + CTA | hero + close | test page nhỏ |
| 1087 | SEOX Clone Home 2026-04-23 | homepage / agency | statement hero | Pool E: Dark Showcase | showcase + cards + proof | hero + close | clone theo mẫu |
| 1082 | Home Native Orange 2026-04-23 | homepage / product marketing | slider hero | Pool A: Slider Commerce | grid card + split section | hero + mid + close | safe pattern gốc |

## Kết Luận Vận Hành

Chuỗi lặp nổi bật hiện tại là:

- `1082`
- `1134`
- `1136`
- `1140`
- `1144`

Điểm chung:

- dùng `slider hero` hoặc biến thể rất gần
- dùng `Pool A`
- đi theo `grid -> split -> process -> FAQ -> CTA`

Từ nay đây là `chuỗi cấm lặp`.

## Chuỗi Tạo Mới Đã Xác Minh

Hai page mới đã chứng minh novelty gate có thể tạo output khác sâu:

- `1150`
- `1148`

Điểm khác biệt:

- không dùng `Pool A`
- không dùng `slider hero`
- không rơi vào `grid -> split -> process -> FAQ -> CTA`
