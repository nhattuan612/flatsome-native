# Factory Flow Handshake Audit Report

Date: 2026-04-25

## Mục Đích

Audit lớp bắt tay giữa:

- `05-flows/`
- `03-factory/`

để kiểm tra:

- flow yêu cầu gì
- factory có trả lời đủ không
- có bước nào bị thiếu `handoff artifact` không

## Kết Luận Nhanh

- có `2` lỗ hở thật ở lớp handshake
- đã sửa ngay
- sau sửa, flow và factory bắt tay rõ hơn ở:
  - `Skeleton`
  - `Archetype`
  - `Section starter direction`
  - `Block reuse decision`
  - `Design Mode` handoff

## Lỗ Hở 1: Block Reuse Chưa Nổi Thành Gate

### Vấn đề

Flow tổng trước đó đã khóa:

- `Skeleton`
- `Archetype`
- `Layout DNA`
- `Layout Pool`
- `Hero Family`

nhưng `block reuse decision` mới chỉ nằm rải trong:

- `Page Goal Routing`
- `Page Plan Template`

chưa nổi lên như một gate rõ trong `Master System Flow Map`.

### Rủi ro

- worker route đúng archetype nhưng vẫn dựng lại section lặp từ đầu
- `Page Plan` có trường reuse nhưng flow không ép đủ mạnh
- block library khó phát triển thành tài sản công ty

### Cách sửa

Đã thêm vào `05-flows/Master System Flow Map.md`:

- `Gate 3B: Block Reuse Gate`
- `Block Reuse Decision`
- ref tới:
  - `03-factory/Block Library Candidates.md`
  - `03-factory/Block Registry.md`
  - `03-factory/Section Archetypes.md`

## Lỗ Hở 2: Factory Bàn Giao Sang Page Plan Chưa Ghi Rõ Gói Handoff

### Vấn đề

`Page Goal Routing` và `Factory Overview` có route tốt, nhưng chưa ghi đủ một gói bàn giao bắt buộc trước khi sang `Page Plan`.

### Rủi ro

- flow yêu cầu `Reuse từ block sẵn có`
- nhưng factory chưa ép worker ghi rõ:
  - `reuse existing block / create new / page-only block`
  - `section starter direction`
  - `Design Mode handoff` nếu task là creative

### Cách sửa

Đã thêm:

#### Trong `03-factory/Page Goal Routing.md`

- `Gói Bàn Giao Factory Bắt Buộc`

#### Trong `03-factory/Factory Overview.md`

- `Factory Handshake Rule`

#### Trong `03-factory/Composition Rules.md`

- rule `decide reuse existing block / create new / page-only block before full Section Map`

#### Trong `03-factory/Block Registry.md`

- `Handshake Với Flow Và Page Plan`

## File Đã Sửa

- `05-flows/Master System Flow Map.md`
- `03-factory/Page Goal Routing.md`
- `03-factory/Factory Overview.md`
- `03-factory/Composition Rules.md`
- `03-factory/Block Registry.md`

## Tác Động Sau Khi Sửa

- flow tổng không còn bỏ sót block governance
- factory không còn bàn giao mơ hồ sang `Page Plan`
- creative route giờ rõ hơn khi đi qua factory
- khả năng tái dùng block được đẩy lên thành quyết định bắt buộc, không còn là ý thích

## Phán Quyết

Sau audit này, lớp `flow -> factory -> page plan` đã chặt hơn ở đúng điểm dễ rơi nhất:

- route đúng nhưng vẫn quên reuse
- route đúng nhưng chưa có handoff artifact rõ
