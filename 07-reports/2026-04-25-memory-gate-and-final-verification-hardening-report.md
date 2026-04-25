# Memory Gate And Final Verification Hardening Report

Date: 2026-04-25

## Mục Đích

Siết lại `2` điểm governance nhỏ nhưng dễ gây lệch vận hành:

- field bằng chứng cuối trong `Final Verification`
- điều kiện cập nhật `07-reports/Recent Page Memory.md`

## Vấn Đề Đã Thấy

### 1. `Final Verification Template` còn dấu vết screenshot như thể là chuẩn mặc định

Điểm lệch:

- hệ đã chốt bỏ yêu cầu `screenshot evidence` như điều kiện pass bắt buộc
- nhưng template vẫn còn field `Screenshot cuối đã có`

Rủi ro:

- worker mới có thể hiểu nhầm screenshot là artifact bắt buộc
- flow core và template verification không còn khớp hoàn toàn

### 2. `Recent Page Memory` còn `1` câu quá rộng

Câu cũ:

- `Mỗi lần hoàn thành page mới phải cập nhật file này`

Rủi ro:

- worker có thể nhét cả page chỉ sửa nhỏ vào novelty memory
- novelty gate bị nhiễu vì dữ liệu so gần nhất không còn sạch

## Cách Sửa

### `06-templates/Final Verification Template.md`

- đổi `Screenshot cuối đã có` thành `Bằng chứng verify cuối`
- thêm:
  - `Quyết định cập nhật Recent Page Memory`
  - `Lý do cập nhật hoặc bỏ qua`

### `07-reports/Recent Page Memory.md`

- thay rule mở đầu bằng điều kiện hẹp hơn:
  - chỉ cập nhật khi page thật sự đáng tham gia novelty gate
- định nghĩa rõ `rebuild đủ lớn`
- thêm danh sách trường hợp `không cập nhật`

### `05-flows/Master System Flow Map.md`

- đồng bộ lại `Gate 8: Memory Update Gate`
- thêm tiêu chí khách quan hơn cho `rebuild đủ lớn`

## Tác Động Sau Khi Sửa

- `Final Verification` không còn kéo worker về tư duy screenshot-bắt-buộc
- quyết định `memory update` được ghi rõ ở artifact cuối
- `Recent Page Memory` sạch hơn, ít bị nhiễu bởi task sửa nhỏ
- novelty gate về sau có dữ liệu so sánh đáng tin hơn

## Kết Luận

Đây là đợt hardening nhỏ, không đổi lõi flow build page, nhưng làm lớp release và novelty governance chặt hơn.
