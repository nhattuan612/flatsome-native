# Layout Pool

Date: 2026-04-24

## Mục Đích

Tài liệu này tồn tại để chặn việc builder tự rơi về `safe pattern` quen thuộc.

`Layout DNA` trả lời trang có tính cách gì.

`Layout Pool` trả lời:

- được phép bắt đầu từ những bố cục lớn nào
- pool nào đang lặp quá nhiều
- pool nào nên ưu tiên để tạo mới lạ

## Luật Cứng

1. Trước khi build, phải chọn `1 Layout Pool`.
2. Không được để trống trường `Layout Pool đã chọn` trong `Page Plan`.
3. Nếu pool đã dùng ở trang gần nhất cùng loại, phải đổi pool hoặc ghi lý do chặn lệch.
4. `Layout Pool` là hard gate, không phải gợi ý mềm.

## Cách Chọn Pool

Trước khi chốt pool, phải nhìn lại:

- `07-reports/Recent Page Memory.md`
- `03-factory/Hero Family Matrix.md`
- `03-factory/No Repeat Law.md`

## Pool Dùng Chung Cho Landing / Sales / Product Marketing

### Pool A: Slider Commerce

- `Hero family:`
  - `slider hero`
- `Dominant geometry:`
  - `grid card + split section`
- `Nhịp chính:`
  - đều và sạch
- `CTA pattern:`
  - `hero + mid + close`
- `Dấu hiệu nhận biết:`
  - slider đầu trang
  - card lợi ích hoặc product cards
  - 1 split story
  - testimonial / FAQ
- `Rủi ro:`
  - rất dễ thành `safe pattern`
- `Quy tắc CEO:`
  - không dùng 2 lần liên tiếp nếu không có lệnh giữ nguyên

### Pool B: Statement Soft Cards

- `Hero family:`
  - `statement hero`
- `Dominant geometry:`
  - `soft cards + layered surface`
- `Nhịp chính:`
  - mở mạnh rồi thả lỏng
- `CTA pattern:`
  - `hero + close`, mid CTA nhẹ
- `Dấu hiệu nhận biết:`
  - hero text lớn
  - card sáng, bo mềm
  - tabs hoặc grouped content
  - testimonial cards
- `Phù hợp:`
  - hướng Fluent
  - các page cần cảm giác dễ chịu

### Pool C: Media Wall Narrative

- `Hero family:`
  - `media wall hero`
- `Dominant geometry:`
  - `collage + staggered image`
- `Nhịp chính:`
  - xen kẽ đậm nhạt
- `CTA pattern:`
  - CTA mềm giữa trang, close CTA rõ
- `Dấu hiệu nhận biết:`
  - nhiều ảnh / media surface
  - section kể chuyện bằng bố cục ảnh
  - ít card nhỏ lặp đều
- `Quy tắc CEO:`
  - dùng khi cần mới lạ mạnh hơn safe pattern

### Pool D: Offset Editorial

- `Hero family:`
  - `offset card hero`
- `Dominant geometry:`
  - `asymmetric offset`
- `Nhịp chính:`
  - nén đầu trang, giãn cuối trang
- `CTA pattern:`
  - `CTA mềm dạng khám phá`
- `Dấu hiệu nhận biết:`
  - card nội dung lệch trục
  - split không đối xứng
  - text hierarchy nổi bật
- `Phù hợp:`
  - about, service, premium storytelling, recruitment

### Pool E: Dark Showcase

- `Hero family:`
  - `product focus hero` hoặc `statement hero`
- `Dominant geometry:`
  - `full width banner + showcase section`
- `Nhịp chính:`
  - dồn cao trào giữa trang
- `CTA pattern:`
  - `hero + close`, middle CTA ít nhưng mạnh
- `Dấu hiệu nhận biết:`
  - 1 section dark nổi bật
  - line-up cards
  - gallery / showcase / proof band
- `Phù hợp:`
  - premium products
  - mood thương hiệu rõ

### Pool F: Tabs-Led Utility

- `Hero family:`
  - `split hero` hoặc `statement hero`
- `Dominant geometry:`
  - `tabs + compact info panels`
- `Nhịp chính:`
  - dày thông tin nhưng chia rõ
- `CTA pattern:`
  - CTA sau mỗi nhóm thông tin
- `Dấu hiệu nhận biết:`
  - tabs là xương sống
  - info panels thay cho nhiều section text dài
- `Phù hợp:`
  - pricing, FAQ-heavy, product explainers

### Pool G: Proof-First

- `Hero family:`
  - `statement hero`
- `Dominant geometry:`
  - `proof band + case cards`
- `Nhịp chính:`
  - mở mạnh rồi chứng minh sớm
- `CTA pattern:`
  - CTA rõ sau proof
- `Dấu hiệu nhận biết:`
  - proof lên rất sớm
  - ít vòng vo
  - phù hợp landing chuyển đổi mạnh

### Pool H: Split Mosaic

- `Hero family:`
  - `split hero`
- `Dominant geometry:`
  - `split 50/50 + mosaic follow-up`
- `Nhịp chính:`
  - xen kẽ sáng tối
- `CTA pattern:`
  - `hero + mid + close`
- `Dấu hiệu nhận biết:`
  - split ngay từ đầu
  - sau đó là mosaic / alternating sections
- `Phù hợp:`
  - service page
  - category storytelling

## Pool Rotation Rule

Nếu có nhiều task liên tiếp:

- không dùng cùng `Layout Pool` cho 2 task gần nhau nếu cùng page type
- nếu pool cũ có `Similarity Risk` cao, pool mới phải khác ít nhất:
  - `hero family`
  - `dominant geometry`
  - `CTA pattern`

## Pool Cấm Dùng Như Mặc Định Vô Thức

Các chuỗi sau bị coi là `safe pattern` rủi ro cao nếu lặp lại:

- `slider hero -> benefits grid -> split story -> process -> testimonial -> faq -> CTA`
- `statement hero -> 3 cards -> split image/text -> testimonial -> CTA`
- `hero -> grid -> split -> process -> FAQ -> CTA`

Nếu build đang tự trôi về các chuỗi này:

- phải dừng
- đổi pool
- ghi lý do vào `Page Plan`

## Kết Luận

`Layout Pool` là bộ chọn đường ray.

Nếu không chốt pool, AI rất dễ quay lại đúng bố cục an toàn đã dùng trước đó.
